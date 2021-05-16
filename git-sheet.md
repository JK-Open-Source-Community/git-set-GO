# git-sheet

we should know
- HEAD
- **how to find issues and how to make pull request**
- repository
- git init
- git log
- git revert
- git clone
- git status
- git rebase
- git stash
- .gitignore
- git installation
- git checkout 
- git branch and delete branch
- gh-pages
- upstream
- emojis and markdown
- commits

### git init

The git init command creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository.

### git status 

The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git.

`git add .` → stage

`git commit -m "this is message"`

`git log`

`git clone http\\:` 


`git branch new-branch`

`git checkout new-branch`

- upstream

    `git push --set-upstream origin new-branch` 

    Configuring a remote for a fork
    You must configure a remote that points to the upstream repository in Git to sync changes you make in a fork with the original repository. This also allows you to sync changes made in the original repository with the fork.
    Open Git Bash.
    List the current configured remote repository for your fork.

    `git remote -v`

    Specify a new remote upstream repository that will be synced with the fork.

     `git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git`

    Verify the new upstream repository you've specified for your fork.
    `git remote -v`

    - hard reset

        ```powershell
        git remote add upstream /url/to/original/repo
        git fetch upstream
        git checkout master
        git reset --hard upstream/master  
        git push origin master --force
        ```

    - rebase

        ```powershell
        git remote add upstream /url/to/original/repo
        git fetch upstream
        git checkout master
        git rebase upstream/master 
        git push origin master
        ```
