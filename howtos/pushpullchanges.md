---
layout: howto
title: How To Push and Pull Commits to a Repository (GitHub Desktop Edition)
---

When you edit your code online or in your text editor, you will be prompted to "commit" your changes -- think of this as "saving" your changes. 

These changes can be viewed by everyone in your collaborative group, if you have one, by *pushing* them changes to your GitHub. In comparison, *pulling* changes means that you are *downloading* commits made by someone else or from another source so that you can view them.

### Committing changes with GitHub desktop

After you've edited your code, you will see all of your changes in a sidebar in GitHub Desktop. The icon located next to each change indicates whether these edits consisted of deleting a file, modifying a file, or adding a file.

Before committing your changes, you will have to describe them so others know what changed:
- Type a brief title describing the changes you just made in the first text box
- If necessary, use the second text box to add a more detailed description

After adding a description, select the "Commit to master" button.

{% include bootstrap/figure.md img="/github/github_commitbaseupload.png" caption="Performing a Commit" alt="Commit action sidebar and adding a commit summary" %}

### Pushing changes to GitHub online

Once you've committed your changes, these pending commits will appear in the "Push origin" box at the top of the window.

Select "Push Origin" to *save* these changes to your online GitHub account and local files.

This step also allows your team members and others to see these changes in your online GitHub repository

{% include bootstrap/figure.md img="/github/github_pushcommittoorigin.png" caption="Pushing Commits to the Origin (GitHub)" alt="Pushing Commits to Origin button" %}

### Pulling Changes from GitHub

When edits were made to your files elsewhere or by others, these pending commits will appear in the "Pull origin" box at the top of the window. This is the same place where you would see "Push Origin". 

Select "Pull Origin" to *apply* these new changes to the local files on your computer. 

You will be now able view these changes from your own GitHub account and when you [generate your site](generatingsite.md) from your text editor.

{:.alert .alert-info}
For more information about the GitHub workflow, see these [GitHub guides](https://help.github.com/en/desktop/contributing-to-projects){:target="_blank"}.
