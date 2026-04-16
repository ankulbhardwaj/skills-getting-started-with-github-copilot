# Day 1: GitHub Basics - File Management Commands

## Initial Setup

### Initialize a new Git repository
```bash
git init
# Example: git init
```
Creates a new `.git` directory in your project to start version control.

### Clone an existing repository
```bash
git clone <repository-url>
# Example: git clone https://github.com/username/my-repo.git
```
Downloads a copy of a remote repository to your local machine.

### Configure Git user (one-time setup)
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
# Example: git config --global user.name "John Doe"
# Example: git config --global user.email "john.doe@example.com"
```
Sets up your Git identity for all commits globally on your machine.

---

## File Management

### Check status of files
```bash
git status
# Example: git status
```
Shows which files are modified, staged, or untracked in your working directory.

### Stage a specific file for commit
```bash
git add <filename>
# Example: git add src/app.py
```
Adds a single file to the staging area (index) to include it in the next commit.

### Stage all changed files
```bash
git add .
# Example: git add .
```
Adds all modified and new files in the current directory to the staging area.

### Stage files matching a pattern
```bash
git add *.js
# Example: git add *.js
# Example: git add src/*.py
```
Stages only files matching the specified pattern (e.g., all JavaScript files).

### Remove a file from staging
```bash
git restore --staged <filename>
# Example: git restore --staged src/app.py
```
Unstages a file that was previously added without removing it from your working directory.

### Delete a file and stage the deletion
```bash
git rm <filename>
# Example: git rm src/old-module.py
```
Removes a file from both your working directory and staging area, marking the deletion for commit.

### Delete a file from Git but keep it locally
```bash
git rm --cached <filename>
# Example: git rm --cached .env
```
Stops tracking a file in Git but keeps it in your working directory (useful for local configs).

### Rename or move a file
```bash
git mv <old-filename> <new-filename>
# Example: git mv src/old-name.py src/new-name.py
```
Renames or moves a file and automatically stages the change.

---

## Committing Changes

### Commit staged files with a message
```bash
git commit -m "Your commit message"
# Example: git commit -m "Add user authentication feature"
```
Creates a snapshot of all staged changes with a concise description.

### Commit all tracked files (skip staging)
```bash
git commit -am "Your commit message"
# Example: git commit -am "Fix bug in payment processing"
```
Stages and commits all modified tracked files in one command.

### Amend the last commit
```bash
git commit --amend -m "Updated commit message"
# Example: git commit --amend -m "Fix typo in last commit"
```
Modifies the last commit message or adds forgotten files to the previous commit.

---

## Remote Repository Operations

### Add a remote repository
```bash
git remote add origin <repository-url>
# Example: git remote add origin https://github.com/username/my-repo.git
```
Links your local repository to a remote GitHub repository named "origin".

### View configured remotes
```bash
git remote -v
# Example: git remote -v
```
Displays all remote repositories associated with your local project with their URLs.

### Remove a remote
```bash
git remote remove <remote-name>
# Example: git remote remove upstream
```
Disconnects a remote repository from your local project.

### Fetch updates from remote
```bash
git fetch origin
# Example: git fetch origin
```
Downloads updates from the remote repository without merging changes into your working directory.

### Pull changes from remote
```bash
git pull origin <branch-name>
# Example: git pull origin main
```
Fetches and automatically merges remote changes into your current branch.

### Push commits to remote
```bash
git push origin <branch-name>
# Example: git push origin main
```
Uploads your local commits to the remote repository on the specified branch.

### Push all branches
```bash
git push --all
# Example: git push --all
```
Pushes all branches in your local repository to the remote.

---

## Viewing History

### View commit history
```bash
git log
# Example: git log
```
Displays a list of all commits with author, date, and commit message.

### View commit history (one line per commit)
```bash
git log --oneline
# Example: git log --oneline
```
Shows a compact view of commit history with shortened commit hashes and messages.

### View specific file's history
```bash
git log <filename>
# Example: git log src/app.py
```
Shows all commits that modified the specified file.

### Show changes in a specific commit
```bash
git show <commit-hash>
# Example: git show a1b2c3d
```
Displays the full details and changes made in a specific commit.

---

## Branching

### List all local branches
```bash
git branch
# Example: git branch
```
Shows all branches in your local repository with the current branch highlighted.

### Create a new branch
```bash
git branch <branch-name>
# Example: git branch feature/login-page
```
Creates a new branch based on the current commit without switching to it.

### Switch to a branch
```bash
git checkout <branch-name>
# Example: git checkout feature/login-page
```
Changes your working directory to the specified branch.

### Create and switch to a new branch
```bash
git checkout -b <branch-name>
# Example: git checkout -b feature/user-profile
```
Creates a new branch and immediately switches to it in one command.

### Delete a local branch
```bash
git branch -d <branch-name>
# Example: git branch -d feature/login-page
```
Removes a branch after its changes have been merged.

### Force delete a local branch
```bash
git branch -D <branch-name>
# Example: git branch -D experimental-feature
```
Forcefully removes a branch even if it hasn't been merged.

---

## Undoing Changes

### Discard changes in a file
```bash
git restore <filename>
# Example: git restore src/app.py
```
Reverts a file to its last committed state, discarding all local changes.

### View differences between working directory and last commit
```bash
git diff
# Example: git diff
```
Shows all unstaged changes in your working directory compared to the last commit.

### Revert a specific commit
```bash
git revert <commit-hash>
# Example: git revert a1b2c3d
```
Creates a new commit that undoes the changes from a specific previous commit.

---

## Tips for VS Code Terminal

- You can run all these commands directly in VS Code's integrated terminal.
- Open the terminal with `Ctrl + ~` (backtick) or `View → Terminal`.
- Navigate to your repository folder before running Git commands.
- Use `pwd` to see your current directory path.
- Use `cd <directory>` to change to a different folder.
