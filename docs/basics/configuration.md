---
title: Setup
parent: Basics
nav_order: 1
---
# Git Setup
{: .no_toc }
When using Git, you'll need to configure your identity so that any pushes are under your account. Furthermore, using Git in an IDE may require alternate setup or usage.

- TOC
{:toc}

---

## View Your Configuration
To view your current Git settings, use the `--list` flag in your command line, as given below:

```bash
$ git config --list
```

This displays a list of all active Git settings, including your name, email, editor, and more. You might see output like:

```bash
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
...
```

If the list is long, the output will appear one screen at a time. This means that all of the configuration settings will not be visible at first. To view the whole output:
- Press `Enter` to scroll line by line.
   - You may need to press this many times to find the setting you're looking for.
- Press `q` to quit and return to the command line.

---

## Identity Configuration
This guide will use global modification of your identity. Doing so lets this identity be used between various programs on your computer.

To change the name associated with your commits, run the following command in your terminal:

```bash
$ git config --global user.name "Your username"
```

As a student, you may also need to set the email for your identity. This can be done with the following:

```bash
$ git config --global user.email "youremail@domain.edu"
```

{: .note}
> Identity can also be set per project. This can be done by running the command in the working directoy for your repository and excluding the `--config` argument. However, this needs to be done for each project and is not recommended if working primarily from one account.

---

## Default Editor Configuration
When editing certain files pertaining to push or merge issues, Git opens these in the default text editor for your computer. For most computers, this default is Vi.

To change this default, the general command is:
```bash
$ git config --global core.editor "text editor name"
```

The text to give for the editor name is not always the editor program name. Included below are the commands for VSCode, Notepad++, and Vim.

- **Visual Studio Code (VSCode):**<br>
```bash
$ git config --global core.editor "code --wait"
```

- **Notepad++:**<br>
```bash
$ git config --global core.editor "'C:/Program Files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```

- **Vim:**<br>
```bash
$ git config --global core.editor "vim"
```

---

## Using Git in IDEs
There are many popular IDEs used for coding, and each handles Git in a different way. Below are links to the Git setup page for a few popular IDEs:

- **VSCode**<br>
VSCode has built-in support for Git. This means that, if Git is installed on your computer, no additional extensions are needed! Opening a folder that is a Git repository will enable Source Control functions automatically.

To clone in VSCode, opening the VSCode Source Control view with no directory open should display the following:

![Image showing VSCode Source Control view with no folder opened](/guide-to-git/assets/images/vscode-clone.png)

From here, clone with the repository URL as normal. Use the built-in Source Control view or the terminal to run your other commands from there!

{: .note}
>  For more information on Git in VSCode, visit the [Visual Studio Code docs](https://code.visualstudio.com/docs/sourcecontrol/overview#_working-in-a-git-repository)!

You may also install an extension such as GitHub Codespaces. Check out [this page](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git) for more details.


- **Eclipse** <br>
To use Git in Eclipse, an extension is needed. There are many our there, but EGit is typically required for students. To learn how to install EGit in eclipse, check out [this tutorial](https://eclipsesource.com/blogs/tutorials/egit-tutorial/).

---

{: .note}
> While IDEs may provide special views for using Git, the commands given in this guide can always be used in a terminal or shell such as Git Bash.

<hr/>

<div style="display: flex; justify-content: space-between;">
  <p>
   
  </p>

  <a href="/guide-to-git/docs/basics/" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     ↑ To Basics
  </a>

  <a href="/guide-to-git/docs/basics/clone.html" 
     style="padding: 6px 12px; border-radius: 4px; text-decoration: none; color: #333; font-weight: 500; transition: background-color 0.2s;" 
     onmouseover="this.style.backgroundColor='#f5f6fa'" 
     onmouseout="this.style.backgroundColor='transparent'">
     Git Clone →
  </a>
</div>