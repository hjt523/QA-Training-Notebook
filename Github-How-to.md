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

- git add . 
! at root,

- git add --all 
! more generally 

!! Adding all the updated files to the next commit

- git add {file}
! Adding a specific file(s) to the next commit

- git add *.txt ! Adds all .txt files etc.

### Setting config in local machine
! Needed to commit changes to the repository

! globally - machine

- git config --global user.name "[USERNAME]"

- git config --global user.email "[EMAIL]"

! Locally - Just this repository

- git config user.name "[USERNAME]"

- git config user.email "[EMAIL]"

### Local Repository Status 
! Check local repository state ( like whats staged / already git add etc)
- git status

### Commiting a Change 
! " save " the staged changes
- git commit -m "[COMMIT_MESSAGE]"

### Pushing Changes (git push)
! Updating remote repository with committed changes
! Remote origin, remote_branch main, for example

- git push -u [REMOTE] [REMOTE_BRANCH] 

### Pulling changes
! The opposite of push, pulling remote changes to local repository

- git pull [REMOTE] [REMOTE_BRANCH]

### Ignoring files

* ignore listed
**/ ignore file or folder in repository

# 2. Forking
! You can copy another persons repository to your github page and make a copy by forking it, top right of a github page
! Then just clone and download it etc, some useful things to know when forking.

- remote -v 
! check status of fork clone
- fetch , push can also be used.

- git remote add upstream [URL] 
! Adds the original fork-ee ( or someone elses fork) as an upstream to update from

- git merge upstream/main
! Merges upstream main to origin main ( local repos)

! Can then push to update your own remote fork.

# 3. Branching
! Branching is pretty nifty, it allows people to start a seperate version of the current code you " branch" off from to tweak without altering the last common version.

![branchdiagram](https://github.com/hjt523/QA-Training-Notebook/blob/5768c68a57fa30f9bd2e2bebcba8031d8e9895e5/imagefolder/Branching.jpeg)


### Making a branch and moving to it
- git branch ! To see current branches

-  git branch [NEW_BRANCH_NAME] ! To create a new branch

! So the new branch will contain everything the branch you branch from does, but allow you to make changes without losing the last working version!

- git checkout [Branch] ! Move to a branch
- git checkout -b [NEW_BRANCH_NAME] ! create and move to a new branch!

### Deleting a branch
! The standard is to deleted a branch once you're done using it to keep the web of what you're doing clean, to do this:

- git branch -d [BRANCH_NAME] ! To delete locally. 

- git push --delete origin [BRANCH_NAME] ! To delete at remote repository


# 4. Merging
! Once we have our nice changes in our branch, and it's (hopefully) all working nicely, we need to merge the branch back into main so that main has the new useful features.

![conflict](https://github.com/hjt523/QA-Training-Notebook/blob/034e3f5e519f59d63d86282fc0b4b5211c118792/Merge%20conflict.jpeg)

- git merge [branch]
! Merge branch into main

! conflicts can happen where the two branches have different data in the same places ( like two slightly different lines in a file), in order to merge these need to be resolved
! Git will add markers into the merge file where the error is that needs to be removed in order for you to then commit the changes and complete the merge.
          
### TO BE CONTINUED ###





