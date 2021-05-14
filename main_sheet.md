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

### Add everything to the staging area and commit:
    git commit -a -m "message"

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

### Create a new branch:
    git branch [new_branch_name]

### Switch to a branch:
    git checkout [branch_name]

### Merge branches:
    git merge [branch_name]

* You merge the branch `branch_name` into the current branch

### Delete a branch
    git branch -d [branch_name]
* Use `-D` if changes were never merged into master


## Remote
Usually with GitHub
### Clone a repository:
    git clone [remote_location] [clone_name]
* `remote_location` is usually the URL of the git repository, but can also be a file path
* `clone_name` is what you want to give the directory in which Git will clone the repository
* The remote address now has the name `origin`

### Get a list of a Git project's remotes:
    git remote -v

### See changes on the remote:
    git fetch
* Will not merge changes from the remote into your local repository
* Will bring the changes onto a remote branch

### Integrate remote branch into local branch:
    git merge origin/[branch_name]

### Push branch up to the remote:
    git push origin [your_branch_name]

### Fetch and merge from remote master branch
    git pull


## Git workflow
1. Fetch and merge changes from the remote
2. Create a branch to work on a new project feature
3. Develop the feature on your branch and commit your work
4. Fetch and merge from the remote again (in case new commits were made while you were working)
5. *Push* your branch up to the remote for review
