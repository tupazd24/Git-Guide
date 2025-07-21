# 📘 Git Guide

A beginner-friendly Git guide with commands, their descriptions, and practical narratives. Each command is documented to help understand its purpose and use case in real-world scenarios.

---

## 🔧 Configuration

### `git config --global user.name "Your Name"`  
### `git config --global user.email "you@example.com"`

**What it does:**  
Sets your name and email so your commits are properly attributed.

**Narrative:**  
Before you start using Git, you tell it who you are. Just like putting your name on your homework, this ensures your commits are properly attributed when working alone or on a team.

---

## 📁 Repository Basics

### `git init`

**What it does:**  
Initializes a new Git repository in the current directory.

**Narrative:**  
When starting a brand-new project, this command sets up a Git repo so you can begin tracking changes.

---

### `git clone <repo-url>`

**What it does:**  
Copies an existing repository from a remote source (like GitHub) to your local machine.

**Narrative:**  
Use this when you're joining an existing project or want to contribute to an open-source codebase.

---

## 💾 Staging & Committing

### `git status`

**What it does:**  
Displays the state of the working directory and staging area.

**Narrative:**  
You run this to check which files are staged, modified, or untracked before making a commit.

---

### `git add <file>`

**What it does:**  
Stages the specified file, making it ready to commit.

**Narrative:**  
When you've updated a file and want to commit just that one, this command targets it specifically.

---

### `git add .`

**What it does:**  
Stages **all** modified and new files in the current directory.

**Narrative:**  
You use this when you've made multiple changes and want to stage them all at once.

---

### `git commit -m "Your message"`

**What it does:**  
Commits the staged changes with a brief message describing the change.

**Narrative:**  
Every time you complete a small chunk of work, you commit it with a descriptive message to track progress.

---

### `git commit -am "Your message"`

**What it does:**  
Stages and commits **already tracked** files in one step.

**Narrative:**  
Perfect when you’ve modified existing files and want to skip the `git add` step.

---

### `git log`

**What it does:**  
Shows a history of commits in the current branch.

**Narrative:**  
You check the log to review your commit history or grab a commit hash for cherry-picking or reverting.

---

## 🔄 Working with Remote Repos

### `git remote -v`

**What it does:**  
Lists the remote repositories associated with the local repo.

**Narrative:**  
Helpful when you need to verify or debug your connection to GitHub or another remote.

---

### `git push`

**What it does:**  
Uploads local commits to the remote repository.

**Narrative:**  
After committing locally, you push to share your changes with the rest of the team or backup your work.

---

### `git pull`

**What it does:**  
Fetches changes from the remote repository and merges them into your current branch.

**Narrative:**  
Use this before you start working to make sure your local repo is up to date.

---

### `git fetch`

**What it does:**  
Downloads changes from the remote repository but doesn't merge them.

**Narrative:**  
Useful when you want to see what's changed upstream without affecting your working branch yet.

---

## 🌿 Branching & Merging

### `git branch`

**What it does:**  
Lists all local branches in the repository.

**Narrative:**  
Use this to see what branches exist and which one you're currently on.

---

### `git branch <branch-name>`

**What it does:**  
Creates a new branch.

**Narrative:**  
You create a new branch to work on a feature or bug fix without disturbing the main code.

---

### `git checkout <branch-name>`

**What it does:**  
Switches to the specified branch.

**Narrative:**  
You use this to move between different lines of development in your project.

---

### `git switch <branch-name>`

**What it does:**  
Also switches branches (a more user-friendly alternative to `checkout`).

**Narrative:**  
A newer, more intuitive command for moving to another branch.

---

### `git merge <branch-name>`

**What it does:**  
Merges changes from the specified branch into the current one.

**Narrative:**  
Once your feature is complete, you merge it back into the main branch.

---

## 🧹 Undoing Changes

### `git reset --soft HEAD~1`

**What it does:**  
Moves the HEAD back by one commit but keeps all changes staged.

**Narrative:**  
Used if you want to modify your last commit message or include more files.

---

### `git reset --mixed HEAD~1`

**What it does:**  
Moves HEAD back by one commit and unstages changes.

**Narrative:**  
Helpful when you accidentally committed too soon and want to restage things properly.

---

### `git reset --hard HEAD~1`

**What it does:**  
Removes the last commit and discards all changes permanently.

**Narrative:**  
Use with caution. This is the nuclear option for cleaning up mistakes.

---

### `git checkout -- <file>`

**What it does:**  
Restores a specific file to the last committed state.

**Narrative:**  
When a change you made isn’t working, this lets you quickly revert that file.

---

### `git restore <file>`

**What it does:**  
Replaces the working directory version of a file with the last committed version.

**Narrative:**  
A safer, clearer alternative to `checkout` for undoing local file changes.

---

## 📦 Stashing

### `git stash`

**What it does:**  
Temporarily shelves changes you've made but aren't ready to commit.

**Narrative:**  
Great for when you need to switch branches quickly without losing your current progress.

---

### `git stash pop`

**What it does:**  
Applies the last stashed changes and removes them from the stash list.

**Narrative:**  
Use this to continue your previous work after handling something urgent.

---

### `git stash apply`

**What it does:**  
Applies stashed changes but **does not** remove them from the stash list.

**Narrative:**  
Ideal when you want to try applying the stash but keep a backup just in case.

---

### `git stash save "message"`

**What it does:**  
Saves your work-in-progress with a custom label.

**Narrative:**  
Useful for organizing multiple stashes with descriptive names.

---

## 🍒 Cherry Picking

### `git cherry-pick <commit-hash>`

**What it does:**  
Applies a specific commit from another branch into your current one.

**Narrative:**  
Perfect for pulling in just one useful change without merging the entire branch.

---

## 🧪 Viewing Differences

### `git diff`

**What it does:**  
Shows changes between your working directory and the last commit.

**Narrative:**  
Check what’s different before committing to make sure you’re not including unintended changes.

---

### `git diff --staged`

**What it does:**  
Shows the differences between staged files and the last commit.

**Narrative:**  
Great for reviewing exactly what you’re about to commit.

---

## ✅ Tips for Success

- Run `git status` often — know what’s going on in your repo.
- Keep commits small and focused — one idea per commit.
- Use clear commit messages so your history is understandable.
- Push your work to a remote regularly.
- Double-check that **each command is committed individually**.
