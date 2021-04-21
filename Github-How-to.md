## Github How to's ( non exhaustive)

This file is here to keep track of git commands that i may forget and need a refresher on function with! May expand to include helpful tips, we'll see i guess!

Index.
- 1. Common commands
- 2. Forking


# 1. Common commands:
!git commands always have git infront 

### Cloning a repository
- git clone {url}
The above creates a copy of the git repository at stated URL on local machine. 

### Staging a change
!Making it so the file(s) is included in the next commit basically

git add . ! at root,
git add --all ! more generally 
!! Adding all the updated files to the next commit

git add {file} ! Adding a specific file(s) to the next commit

git add *.txt ! Adds all .txt files etc.

### Setting config in local machine
! Needed to commit changes to the repository

! globally - machine

git config --global user.name "[USERNAME]"

git config --global user.email "[EMAIL]"

! Locally - Just this repository

git config user.name "[USERNAME]"

git config user.email "[EMAIL]"

### Local Repository Status 
! Check local repository state ( like whats staged / already git add etc)
git status

### Commiting a Change 
! " save " the staged changes
git commit -m "[COMMIT_MESSAGE]"

### Pushing Changes (git push)
! Updating remote repository with committed changes
! Remote origin, remote_branch main, for example

git push -u [REMOTE] [REMOTE_BRANCH] 

### Pulling changes
! The opposite of push, pulling remote changes to local repository

git pull [REMOTE] [REMOTE_BRANCH]

### Ignoring files

* ignore listed
**/ ignore file or folder in repository

# 2. Forking
! You can copy another persons repository to your github page and make a copy by forking it, top right of a github page
! Then just clone and download it etc, some useful things to know when forking.

remote -v # check status of fork clone
fetch , push can also be used.

git remote add upstream [URL] # Adds the original fork-ee ( or someone elses fork) as an upstream to update from

git merge upstream/main # Merges upstream main to origin main ( local repos)

! Can then push to update your own remote fork.

# 3. Branching

### TO BE CONTINUED ###




