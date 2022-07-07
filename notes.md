# The Odin Project - Foundations

Started: 04/07/2022.

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
  - [Introduction to HTML and CSS](#introduction-to-html-and-css)
    - [HTML Elements and Tags](#html-elements-and-tags)
    - [index file](#index-file)
    - [HTML File Structure](#html-file-structure)
      - [DOCTYPE](#doctype)
      - [HTML Element](#html-element)
      - [Head Element](#head-element)
        - [Charset Meta Element](#charset-meta-element)
      - [Title Element](#title-element)
      - [Body Element](#body-element)
    - [Working with Text](#working-with-text)
    - [HTML Comments](#html-comments)
    - [HTML Lists](#html-lists)
    - [HTML Links](#html-links)
    - [HTML Images](#html-images)
  - [CSS Foundations](#css-foundations)
    - [Div Tags](#div-tags)
    - [Selectors](#selectors)
      - [Universal Selector](#universal-selector)
      - [Type Selectors](#type-selectors)
      - [Class Selectors](#class-selectors)
      - [ID Selectors](#id-selectors)
      - [Grouping Selectors](#grouping-selectors)
    - [Adding CSS to HTML](#adding-css-to-html)
      - [External CSS (CSS File)](#external-css-css-file)
      - [Internal CSS](#internal-css)
      - [Inline CSS](#inline-css)
    - [Box Model](#box-model)
    - [Block vs Inline](#block-vs-inline)
  - [FlexBox](#flexbox)
    - [FlexBox Resizing](#flexbox-resizing)
    - [FlexBox Axes](#flexbox-axes)
    - [FlexBox Alignment](#flexbox-alignment)

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

## Introduction to HTML and CSS

- HTML: This is the structure of a page.
- CSS: Styling of a page.
- JavaScript: Make the page do some fancy stuff.

### HTML Elements and Tags

Elements are pieces of data, such as a sentence or paragraph of text that is enclosed inside of HTML tags. The HTML tags will tell the browser how to present the information to the person reading it. Each tag (typically(there are some exceptions)) has an opening (`<element-name>`) and a closing tag (`</element-name>`).

For example, a basic 'p' tag is used to present data as a paragraph:

``` html
<p>This is some text</p>
```

### index file

You should always name the file with your homepage on as index.html (or index.htm) as most web servers are setup to look for this file by default when a website is accessed without a page specified.

### HTML File Structure

Sample boilerplate file:

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

#### DOCTYPE

``` html
<!DOCTYPE HTML>
```

The DOCTYPE tells the browser what version of HTML the file is based on and render the file using that version. The above example implies the browser should render the file using HTML 5.

#### HTML Element

``` html
<!DOCTYPE html>
<html lang="en">
</html>
```

The `<html></html>` tags are the root element of the document. Everything that is shown on the page will be enclosed in these tags.

The lang attribute is used to aid in SEO and accessibility.

#### Head Element

This element is used for storing meta data about the page, which is helpful for SEO and search engine discovery.

##### Charset Meta Element

The charset meta element is very important as it tells the browser what character encoding to use to render special symbols on the page. utf-8 is typical for English but other languages may be different.

#### Title Element

The title element tags are used to show the title name of the page in your browsers window or tab.

#### Body Element

This is where you place all of the content for the page.

### Working with Text

| Start Element | End Element | Used For | Usage Example |
| :--- | :--- | :--- | :--- |
| `<p>` | `</p>` | Paragraph of text | `<p>hello world</p>` |
| `<h1>` | `</h1>` | Top heading of a page | `<h1>hello world</h1>` |
| `<h2>-<h6>` | `</h2>-</h6>` | Sub-headings of a page | `<h2>hello world</h2>` |
| `<strong>` | `</strong>` | Make text bold | `<strong>hello world</strong>` |
| `<em>` | `</em>` | Emphasise (italicise) some text | `<em>hello world</em>` |
| `<u>` | `</u>` | Underline some text | `<u>hello world</u>` |

### HTML Comments

Comments in an HTML file are done using `<!-- comment goes here -->`. This is multi-line so you can do a comment like the below:

``` html
<!-- This
Is
A
Comment
-->
```

### HTML Lists

There are two types of lists, ordered and unordered.

Unordered lists (`<ol></ol>`) are bullet point lists, whereas ordered lists (`<ul></ul>`) are numbered lists.

To add an item to a list, use the `<li></li>` element, using it one for each item in the list.

For example:

Ordered list:

``` html
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>
```

Unordered list:

``` html
<ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ul>
```

### HTML Links

For linking to other pages / sites, you use the `<a></a>` element tag. To create a link that goes to google.com for example, do the following:

``` html
<a href="https://www.google.com">Click Me To Go To Google.com</a>
```

The text inside the 'a' tags will be what is shown to you and without styling applied, it will be blue and underlined. If you have clicked it before, it will be purple.

href="" tells the browser what page to go to.

There are two types of link:

- Absolute: A link to a page on another website (e.g google.com).
- Relative: A link to a page on your site (about.html).

An example of a relative link is shown below:

``` html
<a href="./pages/about.html">About</a>
```

### HTML Images

Images are contain in a self-closing `<img>` tag. You use it as follows:

``` html
<img src="./images/dog.jpg" alt="A picture of a dog"/>
```

- src= is used to point to the image you wish to use.
- alt= is used to provide a test description of what the image is. It is used for accessibility, SEO and a placeholder in the event that the image cannot be loaded.

## CSS Foundations

### Div Tags

Div tags in HTML are just empty containers that you use to separate parts up for styling purposes.

### Selectors

Selectors refer to HTML elements that the CSS rule will apply to.

#### Universal Selector

Applies to all elements on the page by default and uses the * notation to apply it to all elements. For example, every element should be the colour red:

``` css
* {
  color: red;
}
```

#### Type Selectors

Applies to all elements on a page that are named after it. For example, make all h1 elements blue:

``` css
h1 {
  color: blue;
}
```

#### Class Selectors

Applies to an element (a div for example) that has the class specified. For example, a div with a class specified that will set the color to green:

``` css
.alert-text {
  color: green;
}
```

``` html
<div class="alert-text">
  This text will be green.
</div>
```

Classes can be reused multiple times and you can apply multiple classes to an element, for example `<div class="alert-text text-underline">`.

#### ID Selectors

Applies to a single element on a page and can only be used once. For example:

``` css
#title {
  color: green;
}
```

``` html
<h1 id="title">
  This text will be green.
</h1>
```

Unlike class selectors, id selectors can only be used once and an element can only have one id selector specified.

Note: ID over-rules a class when there is a conflict.

#### Grouping Selectors

If you have multiple selectors that have common attributes, you can group up those attributes and build out the selectors with unique attributes. For example:

``` css
.read,
.unread {
  color: white;
  background-color: black;
}

.read {
  font-size: 12px;
}

.unread {
  font-size: 14px;
}
```

This way, the only differences are the font size that was specified for each selector but each one has the same foreground and background colours.

### Adding CSS to HTML

#### External CSS (CSS File)

``` html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

#### Internal CSS

``` html
<head>
  <style>
    div {
      color: white;
      background-color: black;
    }

    p {
      color: red;
    }
  </style>
</head>
<body>...</body>
```

#### Inline CSS

``` html
<body>
  <div style="color: white; background-color: black;">...</div>
</body>
```

### Box Model

Every element on a web page is a rectangular box. You can see this by setting the border on an element:

``` css
* {
  border: 2px solid red;
}
```

- Padding: Increases the space between the edge of a box and the content inside of it.
- Margin: Increases the space between a box and any others that sit next to it.
- Border: Adds space (even if it’s only a pixel or two) between the margin and the padding

![padding, margin, border](assets/images/box-model.png)

``` css
.box-one {
  padding: 20px;
  border: 2px solid red;
  margin: 20px;
  height: 100px;
  width: 100px;
}
```

In the above example, the element would be 100px x 100px but the total w or h would be 144px x 144px because the padding, border and margin will add to the size. This is called the standard box model.

To reduce it down so that it sticks to the size of the element (100x100), add `box-sizing: border-box;` to the CSS selector. That way, it can only ever be 100px x 100px. This is often called the alternative box model.

### Block vs Inline

By default, web pages are blocked (stacked) atop of each other.

A Div is a block element. A Span is an inline element, meaning it is used inside another element to do some styling change.

## FlexBox

Flexbox is a relatively new way of manipulating elements in CSS.

Flexbox is a way to arrange items into rows or columns. These items will flex (i.e. grow or shrink) based on some simple rules that you can define.

For example, three divs on a page would normally be stacked below each other (block model). You can use flexbox to align them on one row inside a div:

``` html
<div class="flex-container">
  <div class="one"></div>
  <div class="two"></div>
  <div class="three"></div>
</div>
```

``` css
.flex-container {
  display: flex;
}

/* this selector selects all divs inside of .flex-container (called flex items) */
.flex-container div {
  background: peachpuff;
  border: 4px solid brown;
  height: 100px;
  flex: 1;
}
```

In addition, when you resize the page, they will resize as you go, if you use the flex: 1 CSS property.

The flex declaration is actually a shorthand for 3 properties that you can set on a flex item. These properties affect how flex items size themselves within their container.

### FlexBox Resizing

- flex-grow: This CSS property tells the element how much to grow by. 1 is normal and 2 is twice as much. Mainly useful when you need to grow flex items in a container.
- flex-shrink: Similar to grow but shrinking instead. Same format but you can use 0 to imply "don't shrink".
- flex-basis: This sets the initial size of a flex item. Typically, you would use auto.

### FlexBox Axes

By default, the direction for a flex container is horizontal (row) but you can change it to vertical (column).

``` html
<div class="flex-container">
  <div class="one"></div>
  <div class="two"></div>
  <div class="three"></div>
</div>
```

``` css
.flex-container {
  display: flex;
  flex-direction: column;
}

/* this selector selects all divs inside of .flex-container */
.flex-container div {
  background: peachpuff;
  border: 4px solid brown;
  height: 80px;
  flex: 1 1 auto;
}
```

### FlexBox Alignment

To space out elements in a container, add `justify-content: space-between;` to the container class and remove `flex: 1` from the class used by the items in the container. This way they will be evenly spaced out.

Another alignment option is `gap`. This can be used to specify a specific gap between the elements in the container. For example:

``` html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

``` css
.container {
  height: 140px;
  padding: 16px;
  background: plum;
  border: 4px solid indigo;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

.item {
  width: 60px;
  height: 60px;
  border: 4px solid darkslategray;
  background: skyblue;
}
```
