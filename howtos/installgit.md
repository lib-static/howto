---
layout: howto
title: How To Install Git
---

To manage the code and collaborate on developing your project, you need a version control system to keep everything organized. 

[GitHub](https://github.com/) is a cloud [Git](https://git-scm.com/) repository hosting service with features for collaboration and project management.
Think of it as Google Drive for code with super robust "track changes" baked in.

GitHub is the most popular platform for developing and sharing code -- from enterprise software, to hands-on learning, to academic projects.
Thus, it is great to become familiar with the platform so that you can take part in this community.

Code for your project will be stored on GitHub. 
To connect locally, we install Git (the version control software that powers GitHub) and GitHub Desktop (a handy visual way to use Git) on our local computer.

### Step 1: Install Git
- **Windows**
  - Install [Git for Windows](https://git-scm.com/downloads){:target="_blank"} using the default options, *except* when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". This will give you Git, Git Bash, and Git GUI. Git Bash is a terminal that lets you use UNIX style commands and utilities on Windows, and will be used as your default terminal when working with Jekyll.

- **Mac**
  - Mac systems will require the "Xcode Command Line Tools" installed, so open a terminal (search for "terminal" in your Spotlight), type in the command `xcode-select --install`, and follow the prompts. After the install finishes, try typing `git --version`. If you want a newer version of Git, download the official [Mac git installer](https://git-scm.com/downloads){:target="_blank"}.

- **Linux**
  - Install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).

### Step 2: Configure Git

Once Git is installed, we need to configure your information so that it can connect with your GitHub account.

Since Git is a command line application, we will need to open a terminal to give it commands: 
- On **Windows**, search for "Git Bash" 

- On **Mac** and **Linux**, search for "terminal"

Once you have a terminal open, we will need to give it two commands.

1) Set your username so that it matches your GitHub account username:

`git config --global user.name "User Name"`

2) Set your email address so that it matches your GitHub email address:

`git config --global user.email "myemail@gmail.com"`

{:.alert .alert-info}
Your username and email address are recorded with every commit to help ensure integrity and authenticity of the history. Most people keep their email public, however, check GitHub's tips to [hide your email](https://help.github.com/articles/about-commit-email-addresses/){:target="_blank"} if you are concerned about privacy.

If you are new to using Git and GitHub, we'd also recommend you install [GitHub Desktop](https://desktop.github.com/){:target="_blank"} using the default options. This will help you visualize and implement some of the git processes that often seem non-intuitive. 
