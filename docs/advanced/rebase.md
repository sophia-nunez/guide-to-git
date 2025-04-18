---
title: Rebase
parent: Advanced
nav_order: 3
---
# Git Rebase
{: .no_toc}
Rebase is an alternative to merge in Git. This applies your local commits on top of the incoming changes, rewriting the commit history. It’s often used to keep a cleaner, more linear history, especially when working on branches.

{: .warning}
> This page uses branching terminology. We recommend reading our page on [branches](https://sophia-nunez.github.io/guide-to-git/docs/advanced/branches.html) to get familiar with these terms.

<br>
- TOC
{:toc}

---

## Introduction
When working on a project with others, your local branch may fall behind the main branch on the remote repository. `git rebase` lets you take the changes from your branch and apply them *on top of* the latest commits from another branch. This helps create a cleaner commit history by avoiding unnecessary merge commits.

### Rebase vs Merge
There are some key differences between merge and rebase for Git: 
- **Merge** keeps all commit history, including a new merge commit.
    - Preserves the exact history and collaboration
- **Rebase** rewrites history to make it seem like your work was built off the latest main branch, creating a linear timeline.
    - Avoids unnecessary merge commits.
    - Cleans the history timeline.
    - May result in more conflicts if any others are using the previous commit history and try to pull/push.

In group projects, merge is typically preferred in order to maintain the true history of changes made and prevent issues for other collaborators. Rebase is used on more personal branches, such as to clean up your branch history before merging into main.

---

## How to Rebase
For our example, you’ve been working on a branch called `feature-1` while changes were made to the `main` branch.

To rebase your `feature-1` branch onto the latest version of `main`, use `git checkout [branchname]` to switch to the appropriate branch. Once on the correct branch, run the rebase command using:

```bash
$ git checkout feature-1
$ git pull origin main --rebase
```

If you already have the latest commits from main, you add your commits to the top of the commit hisotry. To do this, use:

```bash
$ git rebase main
```

Due to the rewriting of the commit history, a rebase needs to be followed by a force push. This can be done with the following terminal command:

```bash
$ git push --force
```
{: .warning}
> `--force` overwrites history on the remote repository and should be used with caution. Improper use of this argument may lead to loss of data.

---

## Rebase with `git pull`
You can use a `--rebase` flag to automatically rebase when pulling. This is done using the following command:

```bash
$ git pull --rebase
```

<hr/>

<div style="display: flex; justify-content: space-between;">
  <a href="/guide-to-git/docs/advanced/pull-request.html" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     ← Pull Request
  </a>

  <a href="/guide-to-git/docs/advanced/" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     ↑ To Advanced
  </a>

  <a href="/guide-to-git/docs/advanced/reset.html" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     Git Reset →
  </a>
</div>