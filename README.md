# Git cheat sheet

## Basic Git
### Initialize a new repository:
    git init

### Add to staging area:
    git add [filename]

### Check the status of your staging area and working directory:
    git status

### Make a commit:
    git commit -m "message"

### Commit to a remote branch:
    git push -u origin [branchname]

### Difference between working directory and staging area
    git diff

* Can use `git diff [filename]` to see differences for specific file


### Shows a list of all previous commits:
    git log

## Backtracking
Commit you are currently on is the `HEAD` commit
### Display info about the `HEAD` commit:
    git show HEAD

### Git reset using SHA:
    git reset [commit_SHA]
* This sets the `HEAD` commit to the `commit_SHA` commit. 
* `commit_SHA` are the first seven digits of a commit's SHA
* Use `git log` to see SHA's of previous commits

### Remove file from staging area:
    git reset HEAD [filename]
* Will not discard file changes from working directory

### Roll back to previous commit
    git checkout HEAD [filename]
* Changes your working directory to look exactly as it did when you last made a commit

## Branching
### See the branch you are currently on:
    git branch




