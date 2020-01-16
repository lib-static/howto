---
layout: howto
title: How To Push and Pull Commits to a Repository (GitHub Desktop Edition)
---

When you edit your code online or in your text editor, you will be prompted to "commit" your changes -- think of this as "saving" your changes. 

These changes can be viewed by everyone in your collaborative group, if you have one, by *pushing* them changes to your GitHub. In comparison, *pulling* changes means that you are *downloading* commits made by someone else or from another source so that you can view them.

### Step 1: Committing changes with GitHub desktop

After you've edited your code, you will see all of your changes in a sidebar in GitHub Desktop. The icon located next to each change indicates whether these edits consisted of deleting a file, modifying a file, or adding a file.

Before committing your changes, you will have to describe them so others know what changed:
- Type a brief title describing the changes you just made in the first text box
- If necessary, use the second text box to add a more detailed description

After adding a description, select the "Commit to master" button.

{% include bootstrap/figure.md img="/github/github_commitbaseupload.png" caption="Performing a Commit" alt="Commit action sidebar and adding a commit summary" %}

### Pushing Changes to GitHub

1. Once your changes have been committed, you'll see the number of commits next to "Push Origin" on the right of the top bar displaying your repository and branch.

2. Select "Push Origin." This "saves" your changes to your online account and local files. It also allows your changes to be seen by your team members and others through your GitHub repository online.
{% include bootstrap/figure.md img="/github/github_pushcommittoorigin.png" caption="Pushing Commits to the Origin(GitHub)" alt="Pushing Commits to Origin button" %}

### Pulling Changes from GitHub

1. When other members of your team, or edits were made to your files elsewhere, you'll see a number of commits next to "Pull Origin" on the right of the top bar displaying your repository and branch. The same place you would see "Push Origin". 

2. Select "Pull Origin". This allows those changes made elsewhere to be applied to your local files on your computer. You will be able view these edits and changes from your own GitHub account now and when you [generate your site](generatingsite.md) from your text editor.

{:.alert .alert-info}
For more information and guides about the GitHub workflow, see these [GitHub guides](https://help.github.com/en/desktop/contributing-to-projects){:target="_blank"}.
