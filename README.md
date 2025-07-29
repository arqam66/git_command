git command 
---

## 1. **Getting Started with Git**

### Create a New Git Repository

To start using Git in a new project, you need to initialize a repository (repo). This creates a hidden `.git` folder to track your project files.

* **Create a new repository**:

  ```bash
  git init PROJECT_NAME
  ```

  This will initialize a new Git repository for your project in the folder named `PROJECT_NAME`.

### Clone a Repository

If you want to work with an existing repository hosted online (like on GitHub), you can clone it. This copies all the files and the commit history.

* **Clone a repository**:

  ```bash
  git clone YOUR_GIT_URL
  ```

  This command copies the repository to your local machine using the URL of the remote repository.

* **Clone into a specific directory**:

  ```bash
  git clone GIT_URL FOLDER_NAME
  ```

  This will clone the repository into a folder named `FOLDER_NAME` instead of using the default name.

---

## 2. **Working with Branches**

Branches allow you to work on different features or bug fixes in isolation from the main project.

### List Branches

You can list all the branches in your project to see what you're working on.

* **List local branches**:

  ```bash
  git branch
  ```

  This shows all the branches you’ve created in your local repository.

* **List remote branches**:

  ```bash
  git branch --remote
  ```

  This shows the branches available in remote repositories (such as GitHub).

* **List both local and remote branches**:

  ```bash
  git branch -av
  ```

  This shows both local and remote branches and indicates which branch you're currently on.

### Switch Branches

Switching between branches lets you work on different versions of your project.

* **Switch to an existing branch**:

  ```bash
  git checkout BRANCH_NAME
  ```

### Create a New Branch

You can create a new branch and start working on it without affecting the main project.

* **Create and switch to a new branch**:

  ```bash
  git checkout -b NEW_BRANCH
  ```

### Delete a Branch

You may want to delete a branch once it’s merged or no longer needed.

* **Delete a local branch**:

  ```bash
  git branch -d BRANCH_NAME
  ```

* **Delete a remote branch**:

  ```bash
  git push origin --delete BRANCH_NAME
  ```

---

## 3. **Configuring Git**

Configuring Git ensures your commits are correctly attributed to you.

### Set Your Username and Email

Git uses your username and email address to track who made which changes. You can set these globally (for all repositories) or locally (for a specific project).

* **Set your name**:

  ```bash
  git config --global user.name "YOUR_NAME"
  ```

* **Set your email**:

  ```bash
  git config --global user.email "YOUR_EMAIL"
  ```

### Enable Color Output

For better readability in the terminal, you can enable colorized output for Git commands.

* **Enable color UI**:

  ```bash
  git config --global color.ui auto
  ```

---

## 4. **Making Changes to Your Code**

Git helps you track changes to files and manage your workflow.

### Check Status

Before making any changes, it’s good practice to check what’s going on in your repository.

* **Check status**:

  ```bash
  git status
  ```

### Stage Changes

Before you commit your changes, you need to "stage" them. Staging allows you to choose which changes to include in your next commit.

* **Stage a specific file**:

  ```bash
  git add FILE_PATH
  ```

* **Stage all files in the current directory**:

  ```bash
  git add .
  ```

### Commit Changes

After staging, you can commit your changes with a message explaining what’s been done.

* **Commit staged changes**:

  ```bash
  git commit -m "Your commit message"
  ```

### Undo Changes

* **Unstage a file** (but keep changes):

  ```bash
  git reset FILE_PATH
  ```

* **Discard changes** in a file (non-staged):

  ```bash
  git restore FILE_PATH
  ```

---

## 5. **Ignoring Files**

You can create a `.gitignore` file to tell Git which files or folders should not be tracked. This is useful for files like logs, build directories, and system-specific files.

### Example `.gitignore` File

```bash
# Ignore logs folder
logs/

# Ignore Mac system files
.DS_Store

# Ignore node_modules folder (for JavaScript projects)
node_modules/

# Ignore environment variable files
.env
```

---

## 6. **Working with Remotes**

Remote repositories are repositories hosted on platforms like GitHub, GitLab, or Bitbucket. You can link your local repository to these remote repositories.

### List Remotes

To see all remotes linked to your project:

* **List remotes**:

  ```bash
  git remote -v
  ```

### Add a New Remote

You can add a new remote (for example, when you want to push your code to a new repository).

* **Add a new remote**:

  ```bash
  git remote add REMOTE_NAME REMOTE_URL
  ```

### Remove a Remote

To unlink a remote repository:

* **Remove a remote**:

  ```bash
  git remote rm REMOTE_NAME
  ```

---

## 7. **Viewing Logs and History**

Git logs help you track the history of your project.

### Show Commit History

To see all the commits made on the current branch:

* **Show commit history**:

  ```bash
  git log
  ```

### Show Specific Changes in a File

You can track changes made to specific files by showing the commit history for that file.

* **View commit history for a file**:

  ```bash
  git log -p FILE_PATH
  ```

### Pretty Log Format

You can make the log output more readable by using a simple one-line format with a graphical representation.

* **Show pretty log**:

  ```bash
  git log --pretty=oneline --graph --decorate --all
  ```

---

## 8. **Merging and Rebasing**

Merging and rebasing are techniques used to combine changes from different branches.

### Merge Branches

Merging combines changes from one branch into another.

* **Merge one branch into another**:

  ```bash
  git checkout TARGET_BRANCH
  git merge SOURCE_BRANCH
  ```

### Rebase Branches

Rebasing is a way to integrate changes from one branch onto another by rewriting history.

* **Rebase one branch onto another**:

  ```bash
  git checkout TARGET_BRANCH
  git rebase SOURCE_BRANCH
  ```

---

## 9. **Using Stash**

Git stash lets you temporarily save changes without committing them, which is helpful when you need to switch tasks quickly.

### Save Changes to Stash

To save your uncommitted changes:

* **Stash your changes**:

  ```bash
  git stash
  ```

### Apply Stashed Changes

You can apply stashed changes when you’re ready to continue working on them.

* **Apply the most recent stash**:

  ```bash
  git stash pop
  ```

### Discard a Stash

If you no longer need a stash, you can remove it.

* **Remove the most recent stash**:

  ```bash
  git stash drop
  ```

* **Clear all stashes**:

  ```bash
  git stash clear
  ```

---
