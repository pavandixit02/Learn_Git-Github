# 🚀 Learn Git & GitHub

A structured learning repository for understanding **Git & GitHub from Beginner to Advanced level** through practical examples, commands, notes, and hands-on practice.

> 📚 **Learning by Doing — Learn → Practice → Document → Push to GitHub**

---

## 🎯 About This Repository

This repository is created to document my complete journey of learning **Git & GitHub**.

Here I maintain:

* 📖 Git & GitHub concepts
* 💻 Important Git commands
* 🧪 Practical examples
* 🌿 Branching & branch management
* 🔄 Git workflow
* ↩️ Undoing changes
* 🔗 Remote repository operations
* 📝 Git configuration & aliases
* 🚫 `.gitignore`
* 📥 Clone, Fetch & Pull
* 🧩 Git reset, restore & revert
* 📚 Personal notes and HTML-based learning pages

The main goal is to build a **strong practical understanding of Git and GitHub** rather than only memorizing commands.

---

# 🗺️ Git & GitHub Learning Roadmap

## 1. Git Fundamentals

* [x] What is Git?
* [x] What is GitHub?
* [x] Git vs GitHub
* [x] Git Repository
* [x] Working Directory
* [x] Staging Area
* [x] Git Commit
* [x] Basic Git Workflow

### Basic Workflow

```text
Working Directory
       ↓
   git add
       ↓
Staging Area
       ↓
  git commit
       ↓
Local Repository
       ↓
   git push
       ↓
Remote Repository
     GitHub
```

---

# 🌿 2. Git Branch

Branching allows us to work on different features or versions of a project independently.

📁 Learning File:

`Branch/branch.html`

### Topics

* What is a branch?
* Create a branch
* Check branches
* Switch branches
* Rename branches
* Delete branches
* Merge branches
* Branch workflow

### Important Commands

```bash
git branch
git branch -a
git branch <branch-name>
git switch <branch-name>
git switch -c <branch-name>
git branch -m <new-name>
git branch -d <branch-name>
git merge <branch-name>
```

---

# 🔗 3. Git Alias

Git aliases allow frequently used Git commands to be shortened.

📁 Learning File:

`git-alias/alias.html`

### Example

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.st status
```

Instead of:

```bash
git status
```

we can use:

```bash
git st
```

---

# ✏️ 4. Git Amend

`git commit --amend` is used to modify the most recent commit.

📁 Learning File:

`git-amend/amend.html`

### Important Command

```bash
git commit --amend
```

### Common Use Cases

* Correct the latest commit message
* Add forgotten files to the latest commit
* Modify the latest commit before pushing

Example:

```bash
git add forgotten-file.txt
git commit --amend
```

---

# 📥 5. Git Clone

`git clone` is used to create a local copy of a remote repository.

📁 Learning File:

`git-clone/clone.html`

### Basic Syntax

```bash
git clone <repository-url>
```

Example:

```bash
git clone https://github.com/username/repository.git
```

### Basic Flow

```text
GitHub Repository
       ↓
   git clone
       ↓
Local Repository
       ↓
Local Development
```

---

# 🚫 6. Git Ignore

`.gitignore` tells Git which files and directories should not be tracked.

📁 Learning File:

`git-ignore.html`

### Example

```gitignore
node_modules/
.env
*.log
*.tmp
.vscode/
```

### Example Directory

```text
project/
├── src/
├── node_modules/
├── .env
└── .gitignore
```

If `node_modules/` and `.env` are listed in `.gitignore`, Git will ignore them.

---

# 🔄 7. Git Pull & Fetch

Git Fetch and Git Pull are used to get updates from a remote repository.

📁 Learning File:

`git-pull-&-fetch/pull-&-fetch.html`

## Git Fetch

Downloads remote changes without merging them into the current branch.

```bash
git fetch
```

## Git Pull

Downloads remote changes and integrates them into the current branch.

```bash
git pull
```

### Difference

```text
git fetch
     ↓
Download remote changes
     ↓
Review changes
     ↓
Manual merge if required
```

Whereas:

```text
git pull
     ↓
git fetch
     +
git merge/rebase
```

---

# ↩️ 8. Git Reset

Git Reset is used to move `HEAD` and/or modify the staging area and working directory depending on the reset mode.

📁 Learning File:

`git-reset/reset.html`

### Important Commands

```bash
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
```

### Reset Modes

| Mode      | HEAD  | Staging | Working Directory |
| --------- | ----- | ------- | ----------------- |
| `--soft`  | Reset | Keep    | Keep              |
| `--mixed` | Reset | Reset   | Keep              |
| `--hard`  | Reset | Reset   | Reset             |

> ⚠️ `git reset --hard` can permanently discard uncommitted changes. Use it carefully.

---

# ♻️ 9. Git Restore

Git Restore is mainly used to restore files in the working tree or staging area.

📁 Learning File:

`git-restore/restore.html`

### Important Commands

Restore a working-directory file:

```bash
git restore <file>
```

Unstage a file:

```bash
git restore --staged <file>
```

Example:

```bash
git restore index.html
```

---

# ↩️ 10. Git Revert

Git Revert creates a **new commit** that reverses the changes introduced by an earlier commit.

📁 Learning File:

`git-revert/revert.html`

### Command

```bash
git revert <commit-id>
```

### Important Difference

```text
git reset
    ↓
Moves repository history/HEAD

git revert
    ↓
Creates a new commit
that reverses previous changes
```

`git revert` is generally useful when changes have already been shared with a remote repository.

---

# 📁 Project Structure

Current repository structure:

```text
Learn_Git-Github/
│
├── .gitignore
├── README.md
│
├── GG.css
├── GG.js
│
├── learn_G-GH-1.html
│
├── git-ignore.html
│
├── Branch/
│   ├── branch.html
│   └── first.txt
│
├── git-alias/
│   └── alias.html
│
├── git-amend/
│   └── amend.html
│
├── git-clone/
│   └── clone.html
│
├── git-pull-&-fetch/
│   └── pull-&-fetch.html
│
├── git-reset/
│   └── reset.html
│
├── git-restore/
│   └── restore.html
│
└── git-revert/
    └── revert.html
```

---

# 📚 Current Learning Progress

| #  | Topic            | Status      | Notes                     |
| -- | ---------------- | ----------- | ------------------------- |
| 1  | Git Fundamentals | ✅ Completed | Basic concepts            |
| 2  | Branch           | ✅ Completed | Branch management         |
| 3  | Git Alias        | ✅ Completed | Git shortcuts             |
| 4  | Git Amend        | ✅ Completed | Modify latest commit      |
| 5  | Git Clone        | ✅ Completed | Clone remote repositories |
| 6  | Git Ignore       | ✅ Completed | Ignore files/directories  |
| 7  | Git Pull         | ✅ Completed | Get remote changes        |
| 8  | Git Fetch        | ✅ Completed | Fetch remote changes      |
| 9  | Git Reset        | ✅ Completed | Reset repository state    |
| 10 | Git Restore      | ✅ Completed | Restore files             |
| 11 | Git Revert       | ✅ Completed | Reverse commits           |

---

# 🧠 Important Git Commands

## Repository Setup

```bash
git init
git clone <url>
```

## Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

## Check Repository Status

```bash
git status
```

## Add Files

```bash
git add <file>
git add .
```

## Commit

```bash
git commit -m "commit message"
```

## View History

```bash
git log
git log --oneline
git log --graph --oneline --all
```

## Remote Repository

```bash
git remote -v
git remote add origin <url>
git push -u origin main
git push
git pull
git fetch
```

## Branches

```bash
git branch
git branch -a
git switch <branch>
git switch -c <branch>
git merge <branch>
git branch -d <branch>
```

---

# 🔄 Complete Git Workflow

A common Git + GitHub workflow:

```text
              GitHub
                 ↑
              git push
                 ↑
          Local Repository
                 ↑
            git commit
                 ↑
           Staging Area
                 ↑
             git add
                 ↑
          Working Directory
```

### Typical Commands

```bash
git status

git add .

git commit -m "Add new feature"

git push origin main
```

---

# 🌎 Local Repository vs Remote Repository

```text
┌─────────────────────────────┐
│       Local Computer        │
│                             │
│ Working Directory           │
│          ↓                  │
│ Staging Area                │
│          ↓                  │
│ Local Repository            │
└─────────────┬───────────────┘
              │
           git push
              ↓
┌─────────────────────────────┐
│          GitHub              │
│      Remote Repository       │
└─────────────────────────────┘
```

For downloading remote changes:

```text
GitHub
  ↓
git fetch / git pull
  ↓
Local Repository
```

---

# 🛠️ Tools Used

* Git
* GitHub
* VS Code
* HTML
* CSS
* JavaScript
* Linux / Ubuntu
* Git Bash / Terminal

---

# 🎯 Learning Method

For every Git/GitHub topic, I follow this approach:

```text
1. What is it?
       ↓
2. Why is it used?
       ↓
3. How does it work?
       ↓
4. Syntax
       ↓
5. Practical Example
       ↓
6. Real-world Use Case
       ↓
7. Common Mistakes
       ↓
8. Interview Questions
       ↓
9. Hands-on Practice
       ↓
10. Documentation
```

---

# 🚀 Upcoming Topics

The repository will be continuously updated with more advanced Git & GitHub concepts.

### Git

* [ ] Git Tags
* [ ] Git Stash
* [ ] Git Diff
* [ ] Git Log Advanced
* [ ] Git Cherry-pick
* [ ] Git Rebase
* [ ] Git Reflog
* [ ] Git Bisect
* [ ] Git Worktree
* [ ] Git Hooks
* [ ] Git Submodules
* [ ] Git Archive
* [ ] Git Blame

### Branching & Collaboration

* [ ] Feature Branch Workflow
* [ ] Git Merge Strategies
* [ ] Merge Conflicts
* [ ] Rebase Workflow
* [ ] Pull Requests
* [ ] Code Review
* [ ] Protected Branches

### GitHub

* [ ] GitHub Repository Management
* [ ] Pull Requests
* [ ] Issues
* [ ] Labels
* [ ] Milestones
* [ ] Projects
* [ ] GitHub Actions
* [ ] GitHub Pages
* [ ] Releases
* [ ] Secrets & Variables
* [ ] Branch Protection Rules
* [ ] GitHub CLI
* [ ] SSH Authentication
* [ ] Personal Access Token (PAT)

### Advanced GitHub / DevOps

* [ ] GitHub Actions CI/CD
* [ ] Automated Testing
* [ ] Docker + GitHub
* [ ] GitHub Actions + Docker
* [ ] GitHub Actions + AWS
* [ ] GitHub Actions + Kubernetes
* [ ] GitOps
* [ ] CI/CD Pipeline Project

---

# 🧪 Practical Projects

The next phase of this repository will focus on practical projects rather than only individual commands.

### Project 1 — Git Workflow Project

```text
Create Repository
       ↓
Create Branch
       ↓
Make Changes
       ↓
git add
       ↓
git commit
       ↓
git push
       ↓
Pull Request
       ↓
Merge
```

### Project 2 — GitHub CI/CD

```text
Developer
    ↓
Git Push
    ↓
GitHub
    ↓
GitHub Actions
    ↓
Build
    ↓
Test
    ↓
Docker Build
    ↓
Deploy
```

### Project 3 — DevOps Git Workflow

```text
Git
 ↓
GitHub
 ↓
GitHub Actions
 ↓
Docker
 ↓
AWS
 ↓
Deployment
 ↓
Monitoring
```

---

# 💡 Git Learning Philosophy

> **Don't just memorize Git commands — understand what happens inside Git.**

For every command, the goal is to understand:

```text
Command
   ↓
Purpose
   ↓
Internal Git Behavior
   ↓
Repository State
   ↓
Real-world Use
```

---

# 📈 Progress

```text
Git Basics          ████████████████████ 100%
Branching           ████████████████████ 100%
Basic Git Commands  ████████████████████ 100%
Undo Operations     ████████████████████ 100%
Remote Operations   ████████████████████ 100%
Advanced Git        ████░░░░░░░░░░░░░░░░ 20%
GitHub              ████████░░░░░░░░░░░░ 40%
GitHub Actions      ░░░░░░░░░░░░░░░░░░░░ 0%
GitOps              ░░░░░░░░░░░░░░░░░░░░ 0%
```

> Progress will be updated as new topics are learned and documented.

---

# 📌 Repository

**GitHub Repository:**
https://github.com/pavandixit02/Learn_Git-Github

---

# 👨‍💻 Author

**Pavan Kumar Dixit**

BCA Graduate | RHCSA | RHCE | Cloud & DevOps Learner

Currently learning:

```text
Linux
  ↓
Git & GitHub
  ↓
Docker
  ↓
Kubernetes
  ↓
CI/CD
  ↓
Cloud
  ↓
DevOps
  ↓
Cloud & DevOps Projects
```

---

## ⭐ Learning Goal

Build strong practical knowledge of:

**Git → GitHub → CI/CD → Docker → Kubernetes → Cloud → DevOps**

and document the complete learning journey through practical projects and notes.
