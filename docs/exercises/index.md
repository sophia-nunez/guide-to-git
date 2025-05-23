---
title: Exercises
layout: default
nav_order: 5
---
Here are some exercises to apply what you've learned from the guide! You can work in any repository you'd like - we recommed following the exercises in order within the same repository.

- TOC
{:toc}

---
# [Basics](https://sophia-nunez.github.io/guide-to-git/docs/basics/)
## Exercise 0: Configure Git
Set up your Git identity! This includes materials from our [Setup](https://sophia-nunez.github.io/guide-to-git/docs/basics/configuration.html#identity-configuration) page.

**Instructions**
1. Configure your username.
2. Configure your email.
3. Display these.

<details markdown="block">
<summary>💡 Show Solution</summary>

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list
```

Your final result should look similar to the following:
    ![Image of console output displaying configurations](/guide-to-git/assets/images/Ex0/bash-output.png)
</details>

## Exercise 1: Make your repository
Create a private Git repository to track your work on GitHub. This uses content from our [Privacy](https://sophia-nunez.github.io/guide-to-git/docs/intermediate/privacy.html#repository-privacy) page. Do this exercise from the GitHub page (we're NOT working from the terminal quite yet!).

**Instructions**
1. On GitHub, create a private repository named `practice`.
2. Add a file named `exercise1.txt`.
3. Commit the changes.

<details markdown="block">
<summary>💡 Show Solution</summary>

1. On GitHub, click **New Repository**
2. Name it something, such as `practice`
3. Set the privacy to **private**.
4. Click **Create repository**.
5. To make a file on GitHub from the new repository page, click the text boxed in red as below:
    ![Image of new repository page on GitHub with text to add a file boxed in red](/guide-to-git/assets/images/Ex1/add-file.png)
4. Name this file something, such as `exercise1.txt` and put any text you would like (or none at all!).
5. Click **Commit new file**.
6. Your final result should look similar to the following:
    ![Image of GitHub displaying new repository](/guide-to-git/assets/images/Ex1/GitHub-result.png)
</details>


## Exercise 2: Clone repo
Clone your practice repo and enter the workspace so you can edit its contents locally. This exercise references our [Clone](https://sophia-nunez.github.io/guide-to-git/docs/basics/clone.html) page!

**Instructions**
1. On GitHub, find the cloning URL for your repository.
2. Clone your repository in your command line.
3. Change to the repository folder to edit the contents.

<details markdown="block">
<summary>💡 Show Solution</summary>
1. Find the link to your repo on GitHub (e.g. https://github.com/sophia-nunez/guide-to-git.git)
2. Enter the following commands
```bash
$ git clone <repository URL>
cd [repo-name]
```

3. Your final terminal output should look similar to the following:
    ![Image of console output displaying clone and move to repo locally](/guide-to-git/assets/images/Ex2/bash-output.png)

    Your workspace should have a similar structure as below:
    ![Image of file explorer in the cloned repo's local workspace](/guide-to-git/assets/images/Ex2/local.png)

</details>

## Exercise 3: Push Changes
Make and edit a file, and add this to your remote repository. Use your terminal for this exercise to practice the [basic commands](https://sophia-nunez.github.io/guide-to-git/docs/basics/) of Git!

**Instructions**
1. Create a file called `hello.txt`.
2. Stage the changes.
3. Push to your repository.

<details markdown="block">
<summary>💡 Show Solution</summary>
1. Create the `hello.txt` file in your directory. This can be done using your editor or:
    ```bash
    echo "exercise 3!" > hello.txt
    ```
2. Run `git add hello.txt`
3. Run `git commit -m “Added hello.txt”`
4. Your final terminal output should look similar to the following:
    ![Image of console output displaying configurations](/guide-to-git/assets/images/Ex3/bash-output.png)
    Your workspace in the file explorer on your computer should contain the following files:
    ![Image of console output displaying configurations](/guide-to-git/assets/images/Ex3/local-output.png)

    On GitHub, your commits should be displayed in a similar manner to this:
    ![Image of console output displaying configurations](/guide-to-git/assets/images/Ex3/repo-output.png)
</details>

# [Intermediate](https://sophia-nunez.github.io/guide-to-git/docs/intermediate/)
## Exercise 4: Merge Conflicts (solo)
Create a repo for yourself. Add a file called conflict.txt, and then get a [merge conflict](https://sophia-nunez.github.io/guide-to-git/docs/intermediate/merge.html) to occur. Bonus points for solving the conflict!

**Instructions**
1. In your practice repository, add a file called `conflict.txt` and push this to the remote.
2. Cause a merge conflict by editing files on GitHub, then locally.
3. Resolve the conflict and push your local changes.

<details markdown="block">
<summary>💡 Show Solution</summary>
 1. After pushing `conflict.txt`, open this file on GitHub editor by clicking the pencil icon.
 2. Edit the file on GitHub, then click the green **Commit changes** button.
 3. Without pulling, edit the same lines of `conflict.txt` locally from your editor.
 3. Commit the changes using `git add .` and `git commit -m "message here"`:
    ```bash
    git add conflict.txt
    git commit -m "Updated conflict.txt with conflicting edit"
    ```
 4. Attempt to pull using `git pull`. You should see something like this:
    ```bash
    $ git pull
    Auto-merging conflict.txt
    CONFLICT (content): Merge conflict in conflict.txt
    Automatic merge failed; fix conflicts and then commit the result.
    ```
    For example, your terminal might look similar to the following:
    ![Image of console output displaying merge conflict](/guide-to-git/assets/images/Ex4(solo)/bash-conflict.png)

5. Fix the conflict by editing `conflict.txt` in either your IDE or in the command line. This process is demonstrated in detail in the example section of [Merge Conflicts](https://sophia-nunez.github.io/guide-to-git/docs/intermediate/merge.html).
    In the text editor, conflicting lines should be marked similar to the example below:
    ![Image of text editor for conflicting file displaying areas of conflicting changes](/guide-to-git/assets/images/Ex4(solo)/merge-conflict.png)
6. Pushing after fixing the conflict, your terminal output should look similar to the following:
    ![Image of console output displaying resolved push](/guide-to-git/assets/images/Ex4(solo)/bash-resolved.png)
</details>

## Exercise 4: Merge Conflicts (partner)
Create a repository for you and your partner, or use the `practice` one. Cause a [merge conflict](https://sophia-nunez.github.io/guide-to-git/docs/intermediate/merge.html) and try to resolve it. Bonus points for solving the conflict!

**Instructions**
1. Have you and your partner clone the same repository.
2. Add a file called conflict.txt.
3. Have both people edit the file to get a merge conflict to occur.
4. Push each person's change and resolve the conflict.

<details markdown="block">
<summary>💡 Show Solution</summary>
 1. Have you and a partner both clone the same repo and edit the same line in conflict.txt locally.
 2. Ask your partner to push their changes. Now, you try to push your changes via:
 
    ```bash
    git add conflict.txt
    git commit -m "conflicting edit"
    ```
    You should see something like this:
    ```bash
    Auto-merging conflict.txt
    CONFLICT (content): Merge conflict in conflict.txt
    Automatic merge failed; fix conflicts and then commit the result.
    ```
    For example, your terminal might look similar to the following:
    ![Image of console output displaying merge conflict](/guide-to-git/assets/images/Ex4(par)/bash-conflict.png)

2. To fix the conflict, you can either edit conflict.txt in your IDE, or try the following commands:
    ```bash
    # accepting their changes
    git merge --strategy-option theirs
    ```
    Or 
    ```bash
    # keeping our changes
    Git merge –strategy-option ours
    ```

3. Pushing after fixing the conflict, your terminal output should look similar to the following:
    ![Image of console output displaying resolved push](/guide-to-git/assets/images/Ex4(par)/bash-resolved.png)

</details>

# [Advanced](https://sophia-nunez.github.io/guide-to-git/docs/advanced/)
## Exercise 5: Create a branch for a repo and create a PR
Create a repo, or go to your `practice` one, and practice using branches. This refernces our page on [Branches](https://sophia-nunez.github.io/guide-to-git/docs/advanced/branches.html)!

This exercise can be done on GitHub or from the command line. We recommend trying both options - just make two separate files!

**Instructions**
1. Create a branch called `exercise-5`.
2. Add a file called **branch-practice.txt**.
3. Commit and push your changes.
4. Submit a pull request to merge `exercise-5` into main.

<details markdown="block">
<summary>💡 Show Solution</summary>
1. Option 1: GitHub
    1. On the `practice` repository page on GitHub, click **Branch: main** and create a new branch by typing `exercise-5` into the menu.
    2. Click **Add file -> Create new file** and name it `branch-practice.txt`.
    3. In the file contents section, type any text you'd like.
    5. Click **Commit changes**
    6. GitHub should display an option to **Compare & pull request**. Click this and submit the pull request.
    8. Click **Merge pull request** and **Confirm merge**.
2. Option 2: Command Line
    1. Go to your workspace for the repository using `cd [path]`.
    2. Create and switch to the new branch using `git checkout -b exercise-5`.
    3. Create the file in you editor or using the following commands:
        ```bash
        $ echo "Any text you want here" > branch-practice.txt
        $ git add branch-practice.txt
        $ git commit -m "Add branch-practice.txt on exercise-5"
        ```
    5. Push the new branch using `git push -u origin exercise-5`.
    6. After running each of these commands, your terimanl output should look similar to the following:
        ![Image of console output displaying branch creation and modifcation](/guide-to-git/assets/images/Ex5/bash-command.png)
    6. Go to GitHub, where you should see a prompt to open a pull request:
        ![Image of GitHub displaying compare & pull for branch](/guide-to-git/assets/images/Ex5/pull-request.png)
        Click **Compare & pull request**, then **Merge**.
3. After merging, your GitHub page should look similar to the following:
    ![Image of GitHub showing branch merge in the commit history](/guide-to-git/assets/images/Ex5/after-merge.png)
    *Note that the commit history has a merge, and the commit message made on your branch appears in main.*
</details>

## Exercise 6: Fork a repo and create a PR (requires a partner)
Create a repo. Have a partner fork your repo and submit a pull request. This uses material from our page on [Forks](https://sophia-nunez.github.io/guide-to-git/docs/advanced/fork.html)

**Instructions**
1. Fork the repository    
2. Clone this fork
3. Edit a file in the repository
4. Commit and push these changes
5. Submit a pull request and check GitHub

<details markdown="block">
<summary>💡 Show Solution</summary>
1. Have your partner fork your repo on Github
2. Have your partner clone their forked repo using `git clone <their repo url>`.
3. Your partner then must create a new branch using `git checkout -b update(or any name)`
4. Have your partner edit a file in their local repo, for example hello.txt
5. Have your partner commit these changes via
```bash
git add hello.txt
git commit -m "Changed hello.txt"
git push origin update
```
6. After running each of these commands, your terimanl output should look similar to the following:
    ![Image of console output displaying fork creation and modifcation](/guide-to-git/assets/images/Ex6/bash-command.png)
6. Have your partner go on Github and submit a PR:
    ![Image of GitHub displaying compare & pull for fork](/guide-to-git/assets/images/Ex6/pull-request.png)
7. You should see their Pull Request when you enter your repo on GitHub! Your final result should look similar to the following:
    ![Image of GitHub showing fork merge in the commit history](/guide-to-git/assets/images/Ex6/after-merge.png)
    *Note that the commit history has a merge, and the commit message made on your fork appears in main.*
</details>