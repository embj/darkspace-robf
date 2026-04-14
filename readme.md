# The DarkSpace

An educational introduction to the most common Git commands you will use every day.

## git init

`git init` creates a new Git repository in your current directory. This is the first command you
run when starting a new project.

```bash
# Create a new project folder and initialize a Git repository
mkdir my-project
cd my-project
git init
```

After running `git init`, a hidden `.git` folder is created that tracks all of your changes.

## git config

`git config` sets your identity and preferences for Git. You should configure your name and email
before making any commits.

```bash
# Set your name and email globally (applies to all repositories)
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Set your name and email for a single repository only
git config user.name "Your Name"
git config user.email "you@example.com"

# View your current configuration
git config --list
```

## git add

`git add` stages changes so they are ready to be committed. Think of it as telling Git which
changes you want to include in your next snapshot.

```bash
# Stage a single file
git add myfile.txt

# Stage all changed files in the current directory
git add .

# Stage only files matching a pattern
git add *.py
```

## git commit

`git commit` saves your staged changes as a new snapshot in the repository history. Always include
a meaningful message describing what changed.

```bash
# Commit staged changes with a message
git commit -m "Add homepage layout"

# Stage all tracked files and commit in one step
git commit -am "Fix typo in README"
```

## git remote

`git remote` manages connections to remote repositories (like GitHub). This is how your local
repository knows where to push and pull code.

```bash
# Add a remote named "origin" pointing to a GitHub repository
git remote add origin https://github.com/username/my-project.git

# List all configured remotes
git remote -v

# Remove a remote
git remote remove origin
```

## git push

`git push` uploads your local commits to a remote repository so others can see your work.

```bash
# Push commits on the main branch to the remote named "origin"
git push origin main

# Push and set the upstream branch (useful the first time you push a new branch)
git push -u origin main
```

## git pull

`git pull` downloads changes from a remote repository and merges them into your current branch.
Use this to stay up to date with your team's work.

```bash
# Pull the latest changes from the remote "origin" into your current branch
git pull origin main

# Pull using the default upstream branch
git pull
```

## git merge

`git merge` combines changes from one branch into another. This is typically used to bring a
feature branch into the main branch.

```bash
# Switch to the main branch
git checkout main

# Merge the feature branch into main
git merge feature-branch
```

If both branches changed the same lines, Git will report a **merge conflict**. You will need to
open the affected files, resolve the conflicts manually, and then commit the result:

```bash
# After resolving conflicts, stage the resolved files and commit
git add .
git commit -m "Resolve merge conflicts from feature-branch"
```

## Putting It All Together

Here is a typical workflow using these commands:

```bash
# 1. Create and initialize a new project
mkdir my-app && cd my-app
git init

# 2. Configure your identity
git config user.name "Your Name"
git config user.email "you@example.com"

# 3. Create a file and make your first commit
echo "# My App" > README.md
git add README.md
git commit -m "Initial commit"

# 4. Connect to a remote repository and push
git remote add origin https://github.com/username/my-app.git
git push -u origin main

# 5. Later, pull the latest changes from your team
git pull origin main

# 6. Merge a feature branch
git merge feature-login
```
