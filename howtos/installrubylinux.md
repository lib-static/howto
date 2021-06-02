---
layout: howto
title: How To Install Ruby on Linux
tags: Ruby
---

[Ruby](https://www.ruby-lang.org/en/){:target="_blank"} is a fairly young and developing programming language with some unique features. 
To use Jekyll, ***you do not need to know anything about Ruby***, but if you are curious, check out [Ruby in 20 minutes](https://www.ruby-lang.org/en/documentation/quickstart/){:target="_blank"}.
Jekyll requires Ruby version 2.4.0 or above (at the time of this writing), plus a few common build tools. 
Check the [Jekyll requirements](https://jekyllrb.com/docs/installation/) for latest details.

On linux distributions there are a few options for installing [Ruby](https://www.ruby-lang.org/en/): 

- Use a Ruby version manager such as [rbenv](https://github.com/rbenv/rbenv) or [RVM](https://rvm.io/) (**Recommended**, will get you an up to date Ruby version and  a clean environment separated from your system Ruby)
- Use your system Ruby (this is probably out of date and you may not want to mess up your system's environment with new Gems)
- Use your distro's repositories (easy, but will be an out of date version and may introduce some issues where you must install gems as `sudo`).
- Use the official [Ruby snap package](https://snapcraft.io/ruby) maintained by the Ruby core team which stays up-to-date (which may cause some unexpected breakage when updating)

These install methods are outlined below--choose one!
(we generally use rbenv)

## Install Build Tools

First, to install Ruby and Gems (packages for Ruby), you will need some basic build tools (Make and GCC).
Most distributions will have them already installed or will provide a package with everything you will need.
For example, on Ubuntu use `sudo apt install build-essential` to make sure you have everything.

However, some Gems will require additional C extensions to build (you can probably skip this if you are just using Jekyll). 
The [ruby-build](https://github.com/rbenv/ruby-build) provides a [suggested build environment](https://github.com/rbenv/ruby-build/wiki#suggested-build-environment) that can be used for reference.
Updated for Ubuntu 19.10:

```
sudo apt install autoconf bison build-essential libssl-dev libyaml-dev libreadline-dev zlib1g-dev libncurses5-dev libffi-dev libgdbm-dev
```

## Install rbenv and ruby-build

[rbenv](https://github.com/rbenv/rbenv) is Ruby version manager that is seen as a lighter alternative to RVM.
Rbenv only switches versions, so to install Rubies you will also need [ruby-build](https://github.com/rbenv/ruby-build) added as a plugin.

First, install rbenv and ruby-build: 

1. install build dependencies based on the [suggested build environment](https://github.com/rbenv/ruby-build/wiki#suggested-build-environment) from ruby-build (see above).
2. clone rbenv into your home directory: `git clone https://github.com/rbenv/rbenv.git ~/.rbenv`
3. add to PATH (this is for Ubuntu, if using a different distro check the location of your bash profile): `echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc`
4. Close terminal and open a new one.
5. Follow the instructions given by the command `rbenv init` (this can be confusing, because `rbenv init` doesn't do anything, it just prints out the instructions). Or just do this on Ubuntu: `echo 'eval "$(rbenv init -)"' >> ~/.bashrc`
6. Close terminal and open a new one.
7. clone ruby-build into the rbenv plugins directory: `git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build`

Now, you can install a Ruby version using rbenv:

1. Check the [Ruby download page](https://www.ruby-lang.org/en/downloads/) to find the latest stable version or your project requirements to find your desired Ruby version number.
2. Check `rbenv install -l` to get a list of available versions.
3. Use `rbenv install` + version number, e.g.: `rbenv install 2.7.0`. This can take awhile since ruby-build will download and build from source. 
4. Once complete, set the version you want to use: `rbenv global 2.7.0`

Now, `ruby -v` should report what you just set.
If you need a different version for a project, run `rbenv local <version number>` in the directory (which creates a file called `.ruby-version`).

Update rbenv and ruby-build:

Since you installed the tools using git, to update rbenv and ruby-build you simply `git pull` the most recent master branch code.

```
cd ~/.rbenv && git pull
cd "$(rbenv root)"/plugins/ruby-build && git pull
```

**Notes:** 

- The list of available Ruby versions (`rbenv install -l`) is NOT automatically updated, so you should periodically update ruby-build following the git pull method above.
- Gems you install will be specific to the currently used version (global or local). When you install a new gem that includes commands (e.g. Jekyll) rbenv shims have to be rebuilt. This is done automatically (assuming you followed the `rbenv init` instructions), or can be manually triggered with command `rbenv rehash`. 
- There is an Ubuntu package to install, so you can use `sudo apt install rbenv ruby-build`. *Unfortunately* `ruby-build` is *super* out of date, so it will only list very out-of-date versions of Ruby to install. As far as I can tell, this is not a good install method.

## Install Ruby Using RVM

[RVM](http://rvm.io/) is a Ruby version manager, that allows you to install and switch between multiple Ruby versions. 

However, there can be some barriers because the way RVM functions isn't compatible with the default set up of Gnome terminal--either you can reconfigure, or do a little workaround by setting up a second terminal. 

Install curl and build-essential if you don't have them (`sudo apt install curl build-essential`).

Set up Tilix: 

- Install Tilix terminal emulator (`sudo apt install tilix`)
- Open Tilix
- Click on the user name above the terminal window, select Profiles > Edit Profile.
- Click on Command tab, check "Run command as a login shell"
- Close Tilix

Open Tilix and install RVM using the [official instructions](https://rvm.io/rvm/install) (note: there is a [PPA for Ubuntu](https://github.com/rvm/ubuntu_rvm) that can take care of everything).

Install a Ruby version, probably the most recent stable (listed on [Ruby downloads](https://www.ruby-lang.org/en/downloads/)), for example: 
`rvm install 2.7.0`. 
This will download all the dependencies and build the Ruby version, which might take awhile... 

When it completes, check your Ruby, `ruby -v`.
If this is your first version, it will become the default, or you can select one, `rvm use 2.7.0`.
If you want to generate the documentation, run `rvm docs generate-ri`.

Now you can install Jekyll: `gem install bundler jekyll`

Once you restart your system, Gnome terminal will recognize your current Ruby version. 
Use RVM from Tilix.

## Install Ruby Using Repo

Even though the version will not be the most up-to-date, the simplest method is to use your distro's repositories which should automatically pull in dependencies. 
For example, on Ubuntu `sudo apt install ruby-full build-essential zlib1g-dev`, or Fedora `sudo dnf install ruby ruby-devel @development-tools`. 
However, you will want to avoid installing Gems as root user--see the official Jekyll [Ubuntu install docs](https://jekyllrb.com/docs/installation/ubuntu/) for details of a work around that involves modifying your bash profile.

Your Ruby version will be automatically updated if your distro updates the repository (which will generally only be security updates). 

## Install Ruby using Snap

For a more up-to-date version, use the official [Ruby snap package](https://snapcraft.io/ruby) maintained by the Ruby core team.
Install using `sudo snap install ruby --classic` (*note:* the `--classic` flag means the snap will not be "confined", since Ruby will need full access to your system to function. Snaps requiring `--classic` are audited by the repository).

You can also specify a version of Ruby to install using a flag such as `--channel=2.7/stable`.
You may need to install additional build tools as well (at least `build-essential zlib1g-dev`) to install some gems.

Note, if you use `bundle exec` to run commands from Gems, you are good to go--however, you may need to add 

```
eval `ruby.env`
```

to your bash profile (.bashrc) for commands to work without bundler.

Using the snap is a good option if you always use bundler to manage your individual project dependencies.
