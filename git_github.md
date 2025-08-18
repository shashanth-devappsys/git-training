# Git & GitHub Essentials: A Beginner's Guide

Git is a powerful version control system that helps you track changes in your code and collaborate with others. GitHub is a web-based platform that uses Git for version control, providing hosting for software development and version control using Git.

## Git Basic Commands

### 1. `git init`

The `git init` command **initializes a new Git repository** in your current directory. This creates a hidden `.git` folder where Git stores all its version control information. Think of it as telling Git, "Start tracking changes here\!"

**Explanation:** This is the very first step to start using Git in any project.

**Example:**

```bash
# Create a project folder
mkdir my_new_project

# Navigate to your project folder
cd my_new_project

# Initialize a Git repository
git init
```

-----

### 2. `git config`

The `git config` command allows you to **set configuration variables** for your Git environment. This is crucial for identifying yourself in commits.

**Explanation:** You'll typically use this to set your username and email, which will be attached to your commits.

**Examples:**

  * **Setting your username:**
    ```bash
    git config --global user.name "Your Name"
    ```
  * **Setting your email:**
    ```bash
    git config --global user.email "your_email@example.com"
    ```
    The `--global` flag means these settings will apply to all your Git repositories. You can also set project-specific configurations by omitting `--global`.

-----

### 3. `git add`

The `git add` command **stages changes** for the next commit. When you modify files, Git knows about the changes, but they aren't ready to be saved permanently until you "add" them to the staging area.

**Explanation:** It's like preparing files for a snapshot. You're telling Git, "Include these changes in the next save."

**Examples:**

  * **Add a specific file:**
    ```bash
    git add my_document.txt
    ```
  * **Add all changes in the current directory:**
    ```bash
    git add .
    ```
  * **Add all modified and new files recursively:**
    ```bash
    git add --all
    ```

-----

### 4. `git commit`

The `git commit` command **records the staged changes** permanently to the repository history. Each commit is a "snapshot" of your project at a specific point in time and should include a meaningful message explaining the changes.

**Explanation:** This is where you save your work. A good commit message describes *what* you changed and *why*.

**Example:**

```bash
git commit -m "Add initial project structure and README file"
```

The `-m` flag allows you to provide a commit message directly.

-----

### 5. `git branch`

The `git branch` command allows you to **manage branches** in your repository. Branches are independent lines of development. The `main` (or `master`) branch is the default.

**Explanation:** Branches help you work on new features or fixes without affecting the main codebase.

**Examples:**

  * **List all branches:**
    ```bash
    git branch
    ```
  * **Create a new branch:**
    ```bash
    git branch new-feature
    ```
  * **Switch to an existing branch:**
    ```bash
    git checkout new-feature
    # Or for newer Git versions:
    git switch new-feature
    ```
  * **Create a new branch and switch to it immediately:**
    ```bash
    git checkout -b another-feature
    # Or for newer Git versions:
    git switch -c another-feature
    ```

-----

### 6. `git merge`

The `git merge` command **integrates changes from one branch into another**. This is how you combine different lines of development.

**Explanation:** Once you've finished working on a feature in its own branch, you'll typically merge it back into your `main` branch.

**Example:**

```bash
# First, switch to the branch you want to merge *into* (e.g., main)
git checkout main

# Now, merge the 'new-feature' branch into 'main'
git merge new-feature
```

-----

### 7. `git fetch`

The `git fetch` command **downloads commits, files, and refs from a remote repository** into your local repository. However, it **does not merge** these changes into your current working branch.

**Explanation:** It's like "checking for updates" from a remote repository without applying them. It lets you see what changes others have made.

**Example:**

```bash
git fetch origin
```

`origin` is the default name for the remote repository you cloned from.

-----

### 8. `git pull`

The `git pull` command is a convenience command that **downloads content from a remote repository and immediately updates the local repository to match that content**. It's essentially a combination of `git fetch` and `git merge`.

**Explanation:** This is how you get the latest changes from a remote repository and integrate them into your current branch.

**Example:**

```bash
git pull origin main
```

This pulls changes from the `main` branch of the `origin` remote.

-----

### 9. `git push`

The `git push` command **uploads your local commits to a remote repository**. This makes your changes available to others.

**Explanation:** After committing your changes locally, you use `git push` to send them to a platform like GitHub.

**Example:**

```bash
git push origin main
```

This pushes your local `main` branch to the `origin` remote. The first time you push a new branch, you might need to use `--set-upstream` or `-u`:

```bash
git push -u origin new-feature
```

-----

### 10. `git stash`

The `git stash` command **temporarily saves changes that you don't want to commit yet**, allowing you to switch branches or work on something else without committing incomplete work.

**Explanation:** Imagine you're in the middle of a task, and an urgent bug fix comes up. `git stash` lets you put your current changes aside, work on the bug, and then come back to your original task.

**Examples:**

  * **Stash your current changes:**
    ```bash
    git stash save "Work in progress on feature X"
    # Or simply:
    git stash
    ```
  * **List stashes:**
    ```bash
    git stash list
    ```

-----

### 11. `git stash apply`

The `git stash apply` command **reapplies the changes from a stash** onto your current working directory.

**Explanation:** After you've stashed your changes, `git stash apply` brings them back.

**Example:**

```bash
git stash apply
```

If you have multiple stashes, you can specify which one to apply (e.g., `git stash apply stash@{1}`). By default, it applies the most recent stash.

For more adavanced commands list, refer to the following GitHub [gist](https://gist.github.com/shashanth-devappsys/da4eb77cf034cb84313e77ff817db90f)