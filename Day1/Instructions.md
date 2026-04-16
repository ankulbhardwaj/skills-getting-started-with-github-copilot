# Day 1: GitHub Basics - File Management Commands

## Initial Setup

### Initialize a new Git repository
```bash
git init
```
Creates a new `.git` directory in your project to start version control.

### Clone an existing repository
```bash
git clone <repository-url>
```
Downloads a copy of a remote repository to your local machine.

### Configure Git user (one-time setup)
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
Sets up your Git identity for all commits globally on your machine.

---

## File Management

### Check status of files
```bash
git status
```
Shows which files are modified, staged, or untracked in your working directory.

### Stage a specific file for commit
```bash
git add <filename>
```
Adds a single file to the staging area (index) to include it in the next commit.

### Stage all changed files
```bash
git add .
```
Adds all modified and new files in the current directory to the staging area.

### Stage files matching a pattern
```bash
git add *.js
```
Stages only files matching the specified pattern (e.g., all JavaScript files).

### Remove a file from staging
```bash
git restore --staged <filename>
```
Unstages a file that was previously added without removing it from your working directory.

### Delete a file and stage the deletion
```bash
git rm <filename>
```
Removes a file from both your working directory and staging area, marking the deletion for commit.

### Delete a file from Git but keep it locally
```bash
git rm --cached <filename>
```
Stops tracking a file in Git but keeps it in your working directory (useful for local configs).

### Rename or move a file
```bash
git mv <old-filename> <new-filename>
```
Renames or moves a file and automatically stages the change.

---

## Committing Changes

### Commit staged files with a message
```bash
git commit -m "Your commit message"
```
Creates a snapshot of all staged changes with a concise description.

### Commit all tracked files (skip staging)
```bash
git commit -am "Your commit message"
```
Stages and commits all modified tracked files in one command.

### Amend the last commit
```bash
git commit --amend -m "Updated commit message"
```
Modifies the last commit message or adds forgotten files to the previous commit.

---

## Remote Repository Operations

### Add a remote repository
```bash
git remote add origin <repository-url>
```
Links your local repository to a remote GitHub repository named "origin".

### View configured remotes
```bash
git remote -v
```
Displays all remote repositories associated with your local project with their URLs.

### Remove a remote
```bash
git remote remove <remote-name>
```
Disconnects a remote repository from your local project.

### Fetch updates from remote
```bash
git fetch origin
```
Downloads updates from the remote repository without merging changes into your working directory.

### Pull changes from remote
```bash
git pull origin <branch-name>
```
Fetches and automatically merges remote changes into your current branch.

### Push commits to remote
```bash
git push origin <branch-name>
```
Uploads your local commits to the remote repository on the specified branch.

### Push all branches
```bash
git push --all
```
Pushes all branches in your local repository to the remote.

---

## Viewing History

### View commit history
```bash
git log
```
Displays a list of all commits with author, date, and commit message.

### View commit history (one line per commit)
```bash
git log --oneline
```
Shows a compact view of commit history with shortened commit hashes and messages.

### View specific file's history
```bash
git log <filename>
```
Shows all commits that modified the specified file.

### Show changes in a specific commit
```bash
git show <commit-hash>
```
Displays the full details and changes made in a specific commit.

---

## Branching

### List all local branches
```bash
git branch
```
Shows all branches in your local repository with the current branch highlighted.

### Create a new branch
```bash
git branch <branch-name>
```
Creates a new branch based on the current commit without switching to it.

### Switch to a branch
```bash
git checkout <branch-name>
```
Changes your working directory to the specified branch.

### Create and switch to a new branch
```bash
git checkout -b <branch-name>
```
Creates a new branch and immediately switches to it in one command.

### Delete a local branch
```bash
git branch -d <branch-name>
```
Removes a branch after its changes have been merged.

### Force delete a local branch
```bash
git branch -D <branch-name>
```
Forcefully removes a branch even if it hasn't been merged.

---

## Undoing Changes

### Discard changes in a file
```bash
git restore <filename>
```
Reverts a file to its last committed state, discarding all local changes.

### View differences between working directory and last commit
```bash
git diff
```
Shows all unstaged changes in your working directory compared to the last commit.

### Revert a specific commit
```bash
git revert <commit-hash>
```
Creates a new commit that undoes the changes from a specific previous commit.

---

## Tips for VS Code Terminal

- You can run all these commands directly in VS Code's integrated terminal.
- Open the terminal with `Ctrl + ~` (backtick) or `View → Terminal`.
- Navigate to your repository folder before running Git commands.
- Use `pwd` to see your current directory path.
- Use `cd <directory>` to change to a different folder.
