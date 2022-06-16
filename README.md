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

### Skipping the staging area

```bash
git commit -am “Message”
# Commits with a long message
```

### Removeing files

```bash
git rm file1.js 
# Removes from working directory and staging area 
```

```bash
git rm --cached file1.js 
# Removes from staging area only 
```

### Renaming or moving files

```bash
git mv file1.js file1.txt
```

### Viewing the staged/unstaged changes

```bash
git diff 
# Shows unstaged changes
```

```bash
git diff --staged 
# Shows staged changes
```

```bash
git diff --cached 
# Same as the above
```

### Viewing the history

```bash
git log 
# Full history
```

```bash
git log --oneline 
# Summary
```

```bash
git log --reverse 
# Lists the commits from the oldest to the newest
```

### Viewing a commit

```bash
git show 921a2ff 
# Shows the given commit
```

```bash
git show HEAD 
# Shows the last commit
```

```bash
git show HEAD~2 
# Two steps before the last commit
```

```bash
git show HEAD:file.js 
# Shows the version of file.js stored in the last commit
```

### Unstaging files (undoing git add)

```bash
git restore --staged file.js 
# Copies the last version of file.js from repo to index
```

### Discarding local changes

```bash
git restore file.js 
# Copies file.js from index to working directory 
```

```bash
git restore file1.js file2.js 
# Restores multiple files in working directory
```

```bash
git restore . 
# Discards all local changes (except untracked files) 
```

```bash
git clean -fd 
# Removes all untracked files
```

### Restoring an earlier version of a file

```bash
git restore --source=HEAD~2 file.js
```

## Browsing History‌

### Viewing the history 1

```bash
git log --stat 
# Shows the list of modified files
```

```bash
git log --patch 
# Shows the actual changes (patches)
```

### Filtering the history

```bash
git log -3 
# Shows the last 3 entries
```

```bash
git log --author=“Mosh”
```

```bash
git log --before=“2020-08-17”
```

```bash
git log --after=“one week ago”
```

```bash
git log --grep=“GUI” 
# Commits with “GUI” in their message
```

```bash
git log -S“GUI” 
# Commits with “GUI” in their patches 
```

```bash
git log hash1..hash2 
# Range of commits
```

```bash
git log hash1..hash2 
# Range of commits
```

```bash
git log file.txt 
# Commits that touched file.txt
```

### Formatting the log output

```bash
git log --pretty=format:”%an committed %H”
```

### Creating an alias

```bash
git config --global alias.lg “log --oneline"
```

### Viewing a commit 2

```bash
git show HEAD~2
```

```bash
git show HEAD~2:file1.txt 
# Shows the version of file stored in this commit
```

### Comparing commits

```bash
git diff HEAD~2 HEAD 
# Shows the changes between two commits 
```

```bash
git diff HEAD~2 HEAD file.txt 
# Changes to file.txt only
```

### Checking out a commit

```bash
git checkout dad47ed 
# Checks out the given commit 
```

```bash
git checkout master
# Checks out the master branch
```

### Finding a bad commit

```bash
git bisect start
```

```bash
git bisect bad 
# Marks the current commit as a bad commit 
```

```bash
git bisect good ca49180 
# Marks the given commit as a good commit 
```

```bash
git bisect reset 
# Terminates the bisect session
```

### Finding contributors

```bash
git shortlog
```

### Viewing the history of a file

```bash
git log file.txt 
# Shows the commits that touched file.txt
```

```bash
git log --stat file.txt 
# Shows statistics (the number of changes) for file.txt
```

```bash
git log --patch file.txt 
# Shows the patches (changes) applied to file.txt
```

### Finding the author of lines

```bash
git blame file.txt 
# Shows the author of each line in file.txt
```

### Tagging

```bash
git tag v1.0 
# Tags the last commit as v1.0 
```

```bash
git tag v1.0 5e7a828 
# Tags an earlier commit
```

```bash
git tag # Lists all the tags
```

```bash
git tag -d v1.0 # Deletes the given tag
```
