# Git & GitHub Learning Notes

## 1. What is Git?

Git is a Version Control System.

It helps developers:

* track code changes
* save project history
* restore old versions
* collaborate with teams

Think of Git like:

```text
Save points for your project
```

---

# 2. What is GitHub?

GitHub is a cloud platform that stores Git repositories online.

| Git               | GitHub              |
| ----------------- | ------------------- |
| Local tool        | Online platform     |
| Tracks changes    | Stores repositories |
| Works on computer | Works on internet   |

---

# 3. Important Git Workflow

```text
 Working Directory
       ↓
    git add
       ↓
 Staging Area
       ↓
  git commit
       ↓
  Repository
```

---

# 4. Most Important Beginner Concepts

## Repository (Repo)

A project tracked by Git.

---

## Commit

A saved snapshot/version of your project.

---

## Staging Area

Temporary area where changes are prepared before commit.

---

## Branch

A separate timeline/workspace for development.

---

## Merge

Combining branch changes into another branch.

---

## Remote Repository

Online repository stored on GitHub.

---

# 5. Essential Commands

## Check Git Version

```bash
git --version
```

---

## Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@gmail.com"
```

---

## View Git Config

```bash
git config --list
```

---

# 6. Creating a Git Repository

## Create Folder

```bash
mkdir git-practise
cd git-practise
```

---

## Initialize Git

```bash
git init
```

Creates hidden `.git` folder.

---

# 7. Checking File Status

```bash
git status
```

Shows:

* untracked files
* modified files
* staged files

---

# 8. Add Files to Staging Area

## Add Single File

```bash
git add hello.txt
```

## Add All Files

```bash
git add .
```

---

# 9. Commit Changes

```bash
git commit -m "Your message"
```

Example:

```bash
git commit -m "Added hello file"
```

---

# 10. View Commit History

## Full Log

```bash
git log
```

## Short Log

```bash
git log --oneline
```

---

# 11. View Exact Changes

```bash
git diff
```

Shows line-by-line modifications.

---

# 12. GitHub Setup

## Connect Local Repo to GitHub

```bash
git remote add origin REPOSITORY_URL
```

Example:

```bash
git remote add origin https://github.com/username/project.git
```

---

## Verify Remote

```bash
git remote -v
```

---

## Rename Branch to Main

```bash
git branch -M main
```

---

## Push Code to GitHub

```bash
git push -u origin main
```

---

# 13. Clone Repository

Download repository from GitHub.

```bash
git clone REPOSITORY_URL
```

Example:

```bash
git clone https://github.com/username/project.git
```

---

# 14. Pull Latest Changes

```bash
git pull
```

Used to download latest updates from GitHub.

---

# 15. Branching Concepts

## Why Branches Exist

Branches allow developers to:

* work safely
* build features independently
* avoid breaking main project

---

## Main Branch

```text
Stable project version
```

---

## Feature Branch

```text
Separate workspace for new feature
```

---

## Real Example

```text
main
 ├── login-feature
 ├── payment-feature
 └── bug-fix
```

---

# 16. Branch Commands

## View Branches

```bash
git branch
```

---

## Create Branch

```bash
git branch feature1
```

---

## Switch Branch

```bash
git switch feature1
```

OR

```bash
git checkout feature1
```

---

## Merge Branch

```bash
git merge feature1
```

---

# 17. Important Branch Understanding

Branches are:

```text
Separate timelines of commits
```

NOT separate folders.

---

# 18. Merge Conflict

## What is Merge Conflict?

Conflict occurs when:

```text
Two branches modify the same part of a file differently.
```

Git cannot automatically decide which version to keep.

---

# 19. Example Merge Conflict

## Main Branch

```text
Hello Users
```

## Feature Branch

```text
Hello Developers
```

Git becomes confused because same line changed differently.

---

# 20. Conflict Markers

Git inserts markers like:

```text
<<<<<<< HEAD
Main Version
=======
Branch Version
>>>>>>> feature
```

Meaning:

* HEAD → current branch version
* feature → incoming branch version

---

# 21. Resolving Merge Conflict

Developer manually edits file.

Example final content:

```text
Final Version
```

Then:

```bash
git add .
git commit -m "Resolved conflict"
```

---

# 22. Important Interview Answers

## What is Git?

Git is a distributed version control system used to track changes in code.

---

## What is GitHub?

GitHub is a cloud platform used to host Git repositories.

---

## What is a Commit?

A commit is a snapshot/save point of project changes.

---

## Why Use Branches?

Branches allow developers to work independently without affecting stable code.

---

## What is Merge Conflict?

A merge conflict occurs when Git cannot automatically combine changes because the same part of a file was modified differently in multiple branches.

---

# 23. Real Company Workflow

```text
git pull
↓
write code
↓
git add .
↓
git commit
↓
git push
```

Repeated daily.

---

# 24. Very Important Beginner Tips

## Always Check Status

```bash
git status
```

This is your most important command.

---

## Open VS Code Correctly

Inside repository folder:

```bash
code .
```

Ensures:

* terminal
* VS Code
* Git repository

all point to same folder.

---

## Save Files Before Checking Git

Use:

```text
Ctrl + S
```

Unsaved files will not appear in `git status`.

---

# 25. Commands Quick Revision

```bash
git init
git status
git add .
git commit -m "message"
git log
git log --oneline
git diff
git remote add origin URL
git push -u origin main
git clone URL
git pull
git branch
git branch branch_name
git switch branch_name
git merge branch_name
```

---

# 26. Current Learning Status

Completed:

* Git basics
* GitHub basics
* Commits
* Staging area
* Push/Pull
* Clone
* Branching
* Merge
* Merge conflict basics

Next Topics:

* Pull Requests (PR)
* Forking
* Git Ignore
* Undo commands
* Rebase basics
* Real team workflow
* Open source contribution basics
