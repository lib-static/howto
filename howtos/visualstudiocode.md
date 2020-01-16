---
layout: howto
title: How To Install and Set Up Visual Studio Code
---
Visual Studio Code is an open source text editor which will help you develop your CollectionBuilder template. 

It is a simple platform to edit and push collections projects to GitHub, and is a great program to satisfy the first "Software and Installation Setup" step, which is to obtain a viable text editor. 

Though several exist, and will serve CollectionBuilder's function, Visual Studio Code seems to be the most intuitive, versatile, and competent text editor for our purposes. 

### Step 1: Download Visual Studio Code

- Navigate to [Visual Studio Code's website](https://code.visualstudio.com){:target="_blank"}
- Follow the instructions for downloading this program

The website should automatically detect which operating system you're using (Windows, IOS, Linux).

- Select the "Download" button that displays for your computer's operating system 

{% include bootstrap/figure.md img="/visualstudio/screen-shot-1.png" caption="Download buttons for various operating systems" alt="screenshot of the download buttons for Visual Studio Code by operating system" class="w-50" %}

### Step 2: Initiate/finalize the download

After you click on the download button you will be taken to a page that says "Get Started." 

It will also drop a download package to the bottom of your browser (or the top of your browser in the downloads file if using a Mac). 

- Select the downloadeded file and accept the terms of agreement
  - If prompted, follow on-screen instructions such as "click yes, the program is safe" or "are you sure you want to open it"
  
- Select the destination location and menu start folder

- Select any additional tasks (probably only "add to path"), and then install 

{% include bootstrap/figure.md img="/visualstudio/screen-shot-2.png" caption="download file" alt="screen shot of the download file for downloading VS code" class="w-50" %}

After a minute or so the download should be completed and will direct you to click the "finish" button. 

### Step 3: Set up Visual Studio Code 

You will, over time, realize your preferences in Visual Studio Code; however, here are the settings we recommend beginning with when starting Collection Builder. 

#### Update settings to meet CollectionBuilder's needs

- Open Visual Studio Code and scroll down to the gear icon in the bottom left hand corner of the window
{% include bootstrap/figure.md img="/visualstudio/screenshotgears2copy.png" caption="gear icon" alt="screen shot of gear icon" class="w-50" %}

- Select the "Settings" option
{% include bootstrap/figure.md img="/visualstudio/screenshotsettings.png" caption="settings button" alt="screen shot of the settings button" class="w-50" %}

- Near the top right-hand corner of the window, you will see a file icon, select it  
{% include bootstrap/figure.md img="/visualstudio/screenshotfile.png" caption="file icon" alt="screen shot of the file icon" class="w-50" %}

You will then be taken to a tab that contains two curly brackets. *Note*: if there is any text contained inside of the brackets delete it now, but leave the brackets.
{% include bootstrap/figure.md img="/visualstudio/sreenshot.6.png" caption="curly brackets" alt="screen shot of the file icon" class="w-50" %}

- Copy and paste the code below between the two curly brackets

- Save your changes

This will update your settings to what we believe will work compatibly with Collection Builder's needs. 

```
"editor.minimap.enabled": false,  
"editor.wordWrap": "on",  
"html.format.maxPreserveNewLines": 2,  
"html.format.wrapLineLength": 0,  
"editor.codeLens": false,  
"outline.problems.badges": false,  
"outline.problems.enabled": false,  
"outline.problems.colors": false,  
"problems.decorations.enabled": false,  
"problems.autoReveal": false  
```

{% include bootstrap/figure.md img="/visualstudio/screenshot.7.png" caption="copied code" alt="screen shot of pasted text" class="w-50" %}

You have officially *set up* Visual Studio Code!

### Step 4: Add *optional* extensions

You will get used to Visual Studio Code and determine your own preferences over time. Extensions are a great way to customize and maximize your experience coding. 

- Select the "Extensions" icon at the bottom left-hand corner of your window 

{% include bootstrap/figure.md img="/visualstudio/pluginfind.png" caption="extensions icon" alt="screen shot of extensions" class="w-50" %}

A new screen and search bar will appear where you can search for any extensions you want to install. 

{% include bootstrap/figure.md img="/visualstudio/searchbar.png" caption="search bar" alt="screen shot of search bar" class="w-50" %}

#### Search and install plug-ins

Searching and installing plug-ins is as easy as typing in the desired program into your search bar and hitting *enter/return*. 

A few great options when working in CollectionBuilder are:
- Spell check
  - Indicates, with a squiggly and colored line (like in Microsoft Word), when you havre incorrectly spelled something 

- Rainbow CSV
  - Color coordinates your CSV text, helping you stay organized
  
- Avocode
  - Helps when utilizing images edited in Photoshop 

To install one of these extensions, simply search for its name and select the green "install" button. The program will do the rest. 

{% include bootstrap/figure.md img="/visualstudio/spellcheck.png" alt="screen shot of spell check" class="w-50" %}

