---
layout: howto
title: How To Generate your Site from Your Text Editor
---
{:.alert .alert-warning}
<div>
    <p>Before starting this how-to guide, you should already have the following installed:
    <ul>
        <li>a text editor such as <a href="visualstudiocode.html" target="_blank">Visual Studio Code</a> or <a href="installatom.html" target="_blank">Atom</a></li>
        <li><a href="installrubywindows.html" target="_blank">Ruby</a></li>
        <li><a href="installandupdatejekyll.html" target="_blank">jekyll</a></li>
    </ul> 
   </p>
</div>

Generating your website code in your text editor allows you to see your edits as you make them, BEFORE you publish your edits.

### Step 1: Open your repository in your Text Editor

- View this [guide](openrepointexteditor.html) if you're unsure how to do this

### Step 2: Open the terminal in your Text Editor

- View this [guide](openterminalwindows.html) if you're unsure how to do this

### Step 3: Locally serve your website

- Type `jekyll s` into your terminal and hit `enter`
    - This command works with jekyll and acts as a local server for your website
{% include bootstrap/figure.md img="/github/jekylls.png" caption="Locally serving your website" alt="Typing jekyll s into the terminal to locally serve your website" %}

### Step 4: View your website

- After a few seconds, this command will generate a local link for your website
{% include bootstrap/figure.md img="/github/jekyllslink.png" caption="Generating a local link for your website" alt="A screenshot of the local link for your website" %}

- Hold down the `ctrl` button on your keyboard 

- Click on the link displayed after "Server address" to open the website in your browser

{:.alert .alert-success}
Now you can make edits in your text editor and see them in real-time! This means you don't need to push your changes before viewing them.

### Step 5: Make and view further edits

- If you make additional edits in your text editor, save all of your changes and refresh your website to see them

### Step 6: Stop serving your website

- To close your programs or serve another website, go back into your text editor and terminal, type `ctrl + c`, and hit `enter`
