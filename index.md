---
title: Home
layout: home
nav_order: 1
---
# Our Guide
{: .no_toc }
Welcome to our guide to Git! Read below for an introduction to the Git environment, or look at our pages for each command you need to know.

- TOC
{:toc}

---

## Introduction to Git
Git is a **version control system** used to keep track of changes in your code or files over time. This allows developers to modify files while maintaining a history of each change. If anything goes wrong, the work can be recovered by reverting to a previous version.

---

## What is a Repository
A **repository** is a project folder that contains your files and a record of their history. Every Git project is based around a **repository**.

- A **local repository** is stored on your computer and is where you store your changes locally.
- A **remote repository** is stored online (such as on GitHub) and is where you share your changes or get changes made by others.

When using any git commands in your terminal, make sure you are in the workspace for the repository on your computer. This is needed so that the commands can run correctly on the desired project.

{: .note }
> There are additional arguments you can add when running git commands to circumvent this. However, our guide will assume you are in the correct folder.

---

### How Does it Work?
Git works by tracking and saving changes made to files in your local workspace, and then save or share those changes by pushing them to a remote repository online. In general, Git follows a few basic steps that allow your project history to be saved:
1. Modify code in your **working directory**. 
2. *Stage* the files — this tells Git which changes to prepare for saving.
3. *Commit* the staged changes — this saves a snapshot into your **local repository**.
4. *Pull* from the **remote repository**, which updates your local copy with any new commits.
5. *Push* your local commits to the **remote repository**, which adds your changes online to share your work.

Git tracks changes to your files on your computer - this version of the project that is stored on your computer is your **local repository**. When you make a change, you create a *commit* to save a snapshot of your progress at that moment in time. These commits stay local until you *push* them to a **remote repository**. This is an online version of your project hosted on platforms like GitHub. From this remote repository you can back up your work, access it from other devices, and share it with others. You should always *pull* from the remote repository before pushing - this takes any new data or changes from the remote repository and updates your local repsitory accordingly. Pulling ensures that you are up to date on any changes before adding your code.

---

### Terminology
While working with Git, there are some important terms to remember:
- **Repository**: A project folder that Git uses to track changes. This contains your files and the history of your changes.
    - **Local repository**: The version of your repository stored on your own computer.
    - **Remote repository**: A version of you repository stored on the internet (e.g. GitHub).
- **Sections**: Each Git Project is split into three main sections. These are different parts of the project.
    - **Working directory**: Where your project files live on your computer. These are the files that you see and edit.
    - **Staging area (index)**: A holding area to prepare changes before commiting. This tells Git which files you want to the changes of.
    - **.git directory (repository)**: A local, hidden folder where Git stores all of your commits and version history. This is what makes your folder a Git repository. When cloning, this is what is copied.
- **States**: The files in your project move through three different states.
    - **Modified**: The file has been changed but not staged. Git has not been told to track the changes for this file yet.
    - **Staged**: The changed file has been marked to go into your next commit in its current version.
    - **Committed**: The change has been saved in Git's history and is now part of the local repository.

## Command Line Syntax
In this guide, sections of the page are code blocks representing command line input/output. For ease of reading, lines which are user input being with `$`. This sybmol does **not** need to be typed into the terminal when executing the commands.

<hr/>

<div style="display: flex; justify-content: space-between;">
  <p>
   
   </p>

  <p>
   
    </p>

  <a href="/guide-to-git/docs/basics/index.html" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     Basics →
  </a>
</div>