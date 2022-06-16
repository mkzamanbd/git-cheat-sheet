# Git and GitHub Command Cheat Sheet

Git and GitHub Command Cheat Sheet

1. Creating Snapshots‌
    * Initializing a repository
    * Staging files
    * Viewing the status
    * Committing the staged files
    * Skipping the staging area
    * Removing files
    * Renaming or moving files
    * Viewing the staged/unstaged changes
    * Viewing the history
    * Viewing a commit
    * Unstaging files (undoing git add)
    * Discarding local changes
    * Restoring an earlier version of a file

2. Browsing History‌
    * Viewing the history
    * Filtering the history
    * Formatting the log output
    * Creating an alias
    * Viewing a commit
    * Comparing commits
    * Checking out a commit
    * Finding a bad commit
    * Finding contributors
    * Viewing the history of a file
    * Finding the author of lines
    * Tagging

3. Branching & Merging‌
    * Managing branches
    * Comparing branches
    * Stashing
    * Merging
    * Viewing the merged branches
    * Rebasing
    * Cherry picking

4. Collaboration‌
    * Cloning a repository
    * Syncing with remotes
    * Sharing tags
    * Sharing branches
    * Managing remotes

5. Rewriting History‌
    * Undoing commits
    * Reverting commits
    * Recovering lost commits
    * Amending the last commit
    * Interactive rebasing

The essential Git commands every developer must know

This cheat sheet covers all of the Git commands I’ve covered in my Ultimate Git Mastery blog.
✓ Creating snapshots
✓ Browsing history
✓ Branching & merging
✓ Collaboration using Git & GitHub
✓ Rewriting history

## Creating Snapshots‌

### Initializing a repository

```bash
git init 
```

### Staging files

```bash
git add file1.js
# Stages a single file 
```

```bash
git add file1.js file2.js
# Stages multiple files
```

```bash
git add *.js 
# Stages with a pattern
```

```bash
git add . 
# Stages the current directory and all its content
```

### Viewing the status

```bash
git status 
# Full status
```

```bash
git status -s 
# Short status
```

### Committing the staged files

```bash
git commit -m “Message” 
# Commits with a one-line message
```

```bash
git commit 
# Opens the default editor to type a long message
```
