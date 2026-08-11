# Learn README.md Formatting

Learn how to create professional `README.md` files using Markdown, Git, GitHub, code blocks, images, and documentation best practices.

---

## Learning Objectives

By the end of this lesson, you will be able to:

- Create and structure a `README.md` file
- Use Markdown headings, lists, and text formatting
- Create code blocks and inline code
- Add horizontal dividers
- Add and display images
- Organise project files and documentation
- Initialise and manage a Git repository
- Commit changes with Git
- Connect a local repository to GitHub
- Push your project to GitHub

---

## 1. Create a Project Directory

Create a directory for your README project.

```bash
mkdir readme-project
```

Move into the directory:

```bash
cd readme-project
```

---

## 2. Initialise the Git Repository

Initialise Git inside the project directory.

```bash
git init
```

This creates a `.git` directory that Git uses to track changes.

---

## 3. Create the README.md File

Create the Markdown file:

```bash
touch README.md
```

The `.md` extension means that the file uses **Markdown**.

---

## 4. Add a Main Heading

Open `README.md` and add:

````markdown
# My Project
````

The `#` creates a level-1 heading.

---

## 5. Add Subheadings

Use additional `#` characters to create different heading levels.

````markdown
## Overview

### Installation

#### Usage
````

Markdown headings follow this hierarchy:

````text
#       Level 1
##      Level 2
###     Level 3
####    Level 4
````

---

## 6. Add Text

You can write normal paragraphs directly in Markdown.

````markdown
This project demonstrates how to create a professional README.md file.
````

---

## 7. Create an Unordered List

Use `-` to create a bullet list.

````markdown
- Markdown
- Git
- GitHub
- Documentation
````

---

## 8. Create a Numbered List

Use numbers followed by a period.

````markdown
1. Create the project
2. Initialise Git
3. Create README.md
4. Add content
5. Commit the changes
6. Push to GitHub
````

---

## 9. Format Text

### Bold

````markdown
**Important**
````

### Italic

````markdown
*Important*
````

### Bold and Italic

````markdown
***Important***
````

---

## 10. Add a Horizontal Divider

Three hyphens create a horizontal divider:

````markdown
---
````

The three hyphens are typed using the **hyphen/dash key** on your keyboard.

They are commonly referred to as:

> **Horizontal divider** or **horizontal rule**

For example:

````markdown
## Overview

This section explains the project.

---

## Installation

This section explains how to install the project.
````

On GitHub, the `---` renders as a horizontal line.

---

## 11. Add Code Blocks

Use three backticks to create a code block.

````markdown
```bash
git status
```
````

The `bash` tells Markdown that the code is Bash.

It will be rendered as:

```bash
git status
```

You can also specify other languages:

````markdown
```javascript
console.log("Hello World");
```
````

---

## 12. Add Inline Code

Use a single backtick when referring to a command, file, or piece of code inside a sentence.

````markdown
Run the `git status` command to check the repository.
````

This will appear as:

Run the `git status` command to check the repository.

---

## 13. Create an Images Directory

Create a directory for your project images:

```bash
mkdir images
```

Your project should now look like:

````text
readme-project/
├── images/
└── README.md
````

---

## 14. Add Images to the Images Directory

If you have images on your Desktop, copy them into the `images` directory.

For example:

```bash
cp ~/Desktop/git-status.png images/
```

You can copy multiple images at once.

For example, if you want to copy all PNG images from your Desktop:

```bash
cp ~/Desktop/*.png images/
```

You can also copy JPEG images:

```bash
cp ~/Desktop/*.jpg images/
```

Or both:

```bash
cp ~/Desktop/*.{png,jpg,jpeg} images/
```

Check the images directory:

```bash
ls images
```

You should see your images listed.

---

## 15. Add an Image to README.md

Markdown uses the following syntax to display an image:

````markdown
![Git Status](images/git-status.png)
````

The structure is:

````markdown
![Alt Text](Image Path)
````

For example:

````markdown
![Git Status](images/git-status.png)
````

### How it works

- `!` tells Markdown that you are adding an image
- `[Git Status]` is the alternative text
- `(images/git-status.png)` is the path to the image

---

## 16. Organise Your Project

A simple README project can look like this:

````text
readme-project/
├── images/
│   ├── git-status.png
│   ├── staging-area.png
│   └── git-commit.png
└── README.md
````

Keeping images inside an `images/` directory makes the project easier to maintain.

---

## 17. Check Git Status

Check which files Git is tracking.

```bash
git status
```

You may see:

````text
Untracked files:
````

This means Git has detected the files, but they have not yet been added to the staging area.

---

## 18. Add Files to the Staging Area

Add all project files:

```bash
git add .
```

The `.` means:

> Add all changes in the current directory.

Check the status again:

```bash
git status
```

The files should now appear under:

````text
Changes to be committed:
````

---

## 19. Commit Your Changes

Create your first commit:

```bash
git commit -m "initial commit"
```

A commit saves a version of your project in Git.

---

## 20. Create a GitHub Repository

Create a new repository on GitHub.

For example:

````text
readme-project
````

If you already created `README.md` locally, you do not need GitHub to create another README.

---

## 21. Connect Your Local Repository to GitHub

Add the GitHub repository as the remote:

```bash
git remote add origin https://github.com/raphgm/readmelesson2.git
```

---

## 22. Verify the Remote

Check that the remote was added correctly:

```bash
git remote -v
```

You should see:

````text
origin  https://github.com/raphgm/readmelesson2.git (fetch)
origin  https://github.com/raphgm/readmelesson2.git (push)
````

---

## 23. Rename the Branch to main

Rename your current branch:

```bash
git branch -M main
```

---

## 24. Push Your Project to GitHub

Push your project to GitHub:

```bash
git push -u origin main
```

The `-u` sets the upstream branch.

After this, future changes can usually be pushed with:

```bash
git push
```

---

# Final Project Structure

Your project should look similar to:

````text
readme-project/
├── images/
│   ├── git-status.png
│   ├── staging-area.png
│   └── git-commit.png
└── README.md
````

---

# Final Challenge

Create your own professional `README.md`.

Your README must contain:

- A project title
- An overview section
- Multiple heading levels
- An unordered list
- A numbered list
- Bold text
- Italic text
- A horizontal divider
- At least two code blocks
- Inline code
- An `images/` directory
- At least one image
- A project structure section
- Git commands
- A GitHub repository
- At least one Git commit
- The project pushed to GitHub

---

# Complete Git Workflow

Once your README is complete:

```bash
git status
git add .
git commit -m "create professional README"
git branch -M main
git remote add origin https://github.com/raphgm/readmelesson2.git
git push -u origin main
```

---

# What You Learned

In this lesson, you learned how to:

1. Create a `README.md` file
2. Format documentation with Markdown
3. Create headings and lists
4. Format text
5. Create code blocks
6. Create horizontal dividers
7. Add images
8. Organise project files
9. Track files with Git
10. Stage and commit changes
11. Connect Git to GitHub
12. Push your project to GitHub

You have now created and published a professional `README.md` project.
