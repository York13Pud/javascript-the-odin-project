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

### Get Current State of Git Branch

Shows current status of files and commits pending on the current branch.

``` console
git status
```

Examples:

