---
title: Add
parent: Basics
nav_order: 4
---
# Git Add
Once files have been modified in your workspace, you'll need to add these revisions to your [staging area](https://sophia-nunez.github.io/guide-to-git/docs/basics/#terminology). This prepares the files for the version control.

---

## How to Add
When using the `git add` command, you can either add files individually, or all at once. To add one file, do the following in your terminal:

```bash
$ git add [filename]
```

To add all files in the project, use:

```bash
$ git add .
```

After using this command, you shouldn't see any additional output in the terminal. If you would like to check the status of your repository and changes, use [`git status`](https://sophia-nunez.github.io/guide-to-git/docs/intermediate/status.html)

{: .note }
>Using `git add` will add the specified files to the staging area as they are in that moment in time. Further revisions would need to be added again.

<hr/>

<div style="display: flex; justify-content: space-between;">
  <a href="/guide-to-git/docs/basics/clone.html" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     ← Back: Git Clone
  </a>

  <a href="/guide-to-git/docs/basics/" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     ↑ To Basics
  </a>

  <a href="/guide-to-git/docs/basics/commit.html" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     Next: Git Commit →
  </a>
</div>
