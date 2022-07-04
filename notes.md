- [The Odin Project - Foundations](#the-odin-project---foundations)
  - [Introduction](#introduction)
    - [Types of web developers](#types-of-web-developers)
    - [Tiers of developers](#tiers-of-developers)
  - [Learning Process](#learning-process)
  - [Git Commands](#git-commands)
    - [Setup your information](#setup-your-information)
    - [Configure colourful Output](#configure-colourful-output)
    - [Configure Git Global Ignore Files](#configure-git-global-ignore-files)
    - [Clone a GitHub Repo](#clone-a-github-repo)
    - [Get Current State of Git Branch](#get-current-state-of-git-branch)
    - [Adding, Committing and Pushing to GitHub](#adding-committing-and-pushing-to-github)
      - [Add Files](#add-files)
      - [Commit Changes](#commit-changes)
      - [Push The Commit to GitHub](#push-the-commit-to-github)
    - [Git Commit History](#git-commit-history)
  - [Introduction to HTML and CSS.](#introduction-to-html-and-css)

# The Odin Project - Foundations

Started: 04/07/2022.

## Introduction

### Types of web developers

- Front end: Deals mainly with the user interface that viewers of your site browse and interact with.
- Back end: Deals with the systems and services that host the website, such as web servers, databases and API's.
- Full stack: A person that is proficient in both front and back end.

### Tiers of developers

- Junior: Just starting out and likes to build things but may not understand business goals / lingo that well. Does most of the coding.
- Mid-level: Still enjoys building stuff but is more aware of business goals and needs. Still codes a lot.
- Senior-level: More aligned to taking a business problem and coming up with a solution to that problem. Leads a team and is able to interact withe devs and business stakeholders. Does the least coding but still does some. More of a leader / mentor for the developers.

## Learning Process

Simple: Understand it, practice it, and finally teach it!

## Git Commands

### Setup your information

``` console
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
```

### Configure colourful Output

``` console
git config --global color.ui auto
```

### Configure Git Global Ignore Files

``` console
echo .DS_Store >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
```

### Clone a GitHub Repo

``` console
git clone git@github.com:USER-NAME/REPOSITORY-NAME.git
```

### Get Current State of Git Branch

Shows current status of files and commits pending on the current branch.

``` console
git status
```

Example 1: Files added but not committed:

``` console
git status

On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   notes.md
```

Example 2: Files added and committed but not pushed to GitHub:

``` console
git status

On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

Example 3: Current branch is up to date with local branch copy:

``` console
git status

On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

### Adding, Committing and Pushing to GitHub

To get files added / updated in a repository, you need to add them to a commit, commit the changes with a message and then push the commit to GitHub.

#### Add Files

``` console
# Add one file:
git add <name-of-file>

# Add multiple files:
git add <name-of-file-1> <name-of-file-2>

# Add all changed files:
git add .
```

#### Commit Changes

``` console
git commit -m "Put something here about the changes"
```

#### Push The Commit to GitHub

``` console
# To the branch you are actively on:
git push

# To another branch:
git push origin anotherbranch
```

### Git Commit History

To view a list of previous commits, use the below command:

``` console
git log
```

Output:

``` console
commit b6ddef1fcd1a042b7eb0e128a1b28aabff7fae9a
Author: Neil Allwood <neilallwood@icloud.com>
Date:   Mon Jul 4 13:59:38 2022 +0100

    Initial commit. Added notes.md file.

commit 91ad8c0a831b5848935099cd662bef5734a36c40
Author: Neil Allwood <neilallwood@icloud.com>
Date:   Mon Jul 4 10:48:51 2022 +0100

    Updated README file (Typo)

commit 01ef3be8248754bb46e24aaba33fad3de76b3006
Author: dev_neil_a <neilallwood@icloud.com>
Date:   Mon Jul 4 10:42:27 2022 +0100

    Initial commit
```

## Introduction to HTML and CSS.

- HTML: This is the structure of a page.
- CSS: Styling of a page.
- JavaScript: Make the page do some fancy stuff.

