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

# 26. Pull Request (PR)

## What is Pull Request?

A Pull Request (PR) is:

```text
A request to merge one branch into another branch.
```

Usually:

```text
feature branch → main branch
```

---

# Why Pull Requests Exist

Pull Requests are used for:

* code review
* team collaboration
* approval before merge
* discussion on changes
* preventing bad code from entering main branch

---

# Simple Understanding

Instead of directly merging:

```bash
git merge feature1
```

Developers usually:

1. push feature branch to GitHub
2. create Pull Request
3. teammates review code
4. approve changes
5. merge into main

---

# Real Company Workflow

```text
Create branch
↓
Write code
↓
git add .
↓
git commit
↓
git push -u origin branch_name
↓
Create Pull Request on GitHub
↓
Code Review
↓
Approve
↓
Merge into main
```

---

# Important Understanding

## git push

```bash
git push -u origin feature-login
```

ONLY uploads branch to GitHub.

It does NOT merge anything.

---

# Actual Merge Happens After PR Approval

GitHub merges branch after:

* review
* approval
* testing

---

# Difference Between Merge and Pull Request

| Git Merge                | Pull Request                  |
| ------------------------ | ----------------------------- |
| Git command              | GitHub feature                |
| Local operation          | Online collaboration workflow |
| Immediate merge          | Review before merge           |
| Mostly personal projects | Team/company workflow         |

---

# Pull Request Workflow Example

## Step 1 — Create Branch

```bash
git branch login-feature
git switch login-feature
```

---

## Step 2 — Make Changes

Edit files.

---

## Step 3 — Commit Changes

```bash
git add .
git commit -m "Added login feature"
```

---

## Step 4 — Push Branch

```bash
git push -u origin login-feature
```

Meaning:

```text
Upload login-feature branch to GitHub
```

---

## Step 5 — Create Pull Request

On GitHub:

```text
Compare & Pull Request
```

Then:

```text
login-feature → main
```

Meaning:

```text
Request to merge login-feature into main
```

---

# What Happens in PR Review?

Teammates can:

* review code
* comment on lines
* request changes
* approve merge

---

# Why Companies Prefer PRs

Because PRs provide:

✅ safer code
✅ collaboration
✅ review system
✅ cleaner development workflow
✅ easier debugging

---

# Important Interview Answer

## What is Pull Request?

```text
A Pull Request is a request to merge changes from one branch into another branch after review and approval.
```

---

# Simple Analogy

## Direct Merge

```text
Directly adding pages into final assignment.
```

---

## Pull Request

```text
Submitting draft for teacher review before final submission.
```

---

# Important Commands

## Create Branch

```bash
git branch feature-name
```

---

## Switch Branch

```bash
git switch feature-name
```

---

## Commit Changes

```bash
git add .
git commit -m "message"
```

---

## Push Branch

```bash
git push -u origin branch_name
```

---

# Important Concept

PR is NOT replacing merge.

Internally:

```text
Pull Request eventually performs a merge.
```

But with:

* review
* discussion
* approval process added.

---

# 25. `.gitignore`

## Purpose

```text
Ignore files/folders from Git tracking.
```

---

## Example

```text
.env
venv/
node_modules/
__pycache__/
```

---

# Important Rule

`.gitignore` works properly only before file becomes tracked.

---

# 26. `.env` Security

Never upload:
- API keys
- passwords
- tokens

Usually add:

```text
.env
```

inside `.gitignore`.

---

# 27. `git rm --cached`

## Purpose

```text
Stop tracking file but keep it locally.
```

---

## Example

```bash
git rm --cached .env
```

Used when `.env` was accidentally tracked.

---

# 28. Undo Commands

---

# `git restore`

## Purpose

```text
Discard local uncommitted changes.
```

---

## Example

```bash
git restore hello.txt
```

---

# `git restore --staged`

## Purpose

```text
Remove file from staging area without deleting changes.
```

---

## Example

```bash
git restore --staged hello.txt
```

---

# 29. `git reset`

Moves HEAD backward.

HEAD means:

```text
Current/latest commit position
```

---

# `git reset --soft`

## Purpose

```text
Remove commit but keep staged changes.
```

---

## Example

```bash
git reset --soft HEAD~1
```

---

# `git reset --mixed`

## Purpose

```text
Remove commit and unstage files but keep changes.
```

---

## Example

```bash
git reset HEAD~1
```

---

# `git reset --hard`

## Purpose

```text
Remove commits and permanently delete changes.
```

---

## Example

```bash
git reset --hard HEAD~1
```

⚠️ Dangerous command.

---

# 30. `git revert`

## Purpose

```text
Undo committed changes safely without deleting commit history.
```

---

## Important Understanding

`git revert`:
- keeps old commit history
- creates new commit
- removes previous changes safely

---

## Example

```bash
git revert commit_id
```

---

# Difference Between Reset and Revert

| Reset | Revert |
|---|---|
| Removes commits | Keeps history |
| Rewrites history | Creates reverse commit |
| Dangerous in teams | Safe in teams |

---

# 31. Important Daily Workflow

```text
git pull
↓
write code
↓
git status
↓
git add .
↓
git commit -m "message"
↓
git push
```

---

# 32. Most Important Interview Concepts

| Topic | Understanding |
|---|---|
| Commit | snapshot/save point |
| Branch | isolated development timeline |
| Merge | combine branches |
| PR | review before merge |
| Staging Area | ready-to-commit area |
| `.gitignore` | ignore files from tracking |
| Merge Conflict | Git unable to auto-merge |
| Revert | safe undo |
| Reset | move/remove commits |

---

# 33. Current Skill Level

You now understand:

✅ Git basics  
✅ GitHub workflow  
✅ Branching  
✅ Merge conflicts  
✅ Pull Requests  
✅ `.gitignore`  
✅ Undo commands  
✅ Reset vs Revert  
✅ Practical Git workflows
