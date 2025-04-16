---
title: Pull Request
parent: Advanced
nav_order: 2
---

# Pull Requests
{: .no_toc}
Pull requests (PRs) are a way to propose changes to a project on GitHub. Instead of directly merging your changes, you ask others to review and approve them first.

- TOC
{:toc}

---

## Introduction

A **pull request** is a way to ask that your branch or fork be merged into another — typically `main`. It’s commonly used in team projects where code is reviewed before it’s added to the main codebase.

Pull requests show:
- What files and lines of code were changed
- Who made the changes
- Discussion and comments between collaborators
- Whether the branch can be automatically merged or has conflicts

PRs are essential for collaboration because they let others **review**, **test**, and **approve** your code before it’s added. In large projects, the ability to approve requests is typically limited to a few members in the group. This allows these experienced individuals to focus on management.

---

### Terminology

Here are some terms you’ll see when working with pull requests:

- **Pull request (PR)**: A request to merge one branch into another, typically used for code review and approval.
- **Base branch**: The branch you want to merge changes *into* (usually `main`).
- **Compare branch**: The branch containing your changes (e.g., `feature`).
- **Merge**: The process of combining your changes into the base branch.
- **Reviewer**: A teammate or collaborator who looks over the code and suggests improvements or approves the PR.
- **Merge conflict**: When changes in your branch conflict with the base branch and GitHub can’t automatically merge them.
- **Close**: To cancel a pull request without merging it.

---

## How to Submit a Pull Request
Once you’ve pushed your branch to GitHub, you can submit a pull request using the GitHub website:
1. Go to the main page of the repository on GitHub and click on the **Pull Requests** tab.
2. GitHub should suggest your recently pushed branch — click **Compare & pull request**.
    ![Image of compare & pull request button automatically shown on GitHub](/guide-to-git/assets/images/compare-and-pull.png)
    3. Otherwise, click **New pull request**.
    ![Image of new pull request button on GitHub](/guide-to-git/assets/images/pull-request-button.png)
    *Note that the tab selected in the top left of the page is **Pull Requests**.*<br>
4. Choose your **base branch** (usually `main`) and **compare branch** (your feature or debug branch).
5. Review the changes, write a **title** and **description**, then click **Create pull request**:
    ![Image of the Pull Request submission page](/guide-to-git/assets/images/pull-request-submission.png)

With these steps, your PR will be open and ready for feedback or approval.

---

## How to Manage Pull Requests

Once a pull request is submitted, here are a few things that can happen:

- **Approval**: If everything looks good, someone with permission can click **Merge pull request**.
- **Requested changes**: Reviewers might leave comments or request updates. You can make changes in your branch and commit them, and they will automatically appear in the same PR.
- **Update with `main`**: If `main` has changed since you created your branch, you might need to **merge** or **rebase** to update your PR. This will allow you to define how you want areas of conflicting edits to be resolved if your changes are approved.
    - **Resolve merge conflicts**: If your PR has conflicts, GitHub will show a message. You’ll need to fix these locally or in the browser.

To close a pull request without merging (for example, if it’s no longer needed), go to the pull request and click **Close pull request**.

