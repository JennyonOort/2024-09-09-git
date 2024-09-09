# 2024-09-09-git: History and Conflicts

`git add .` 
- add all files in the current working directory
- best practice is always to check the appropriate files has been added with git status

`git remote add <NAME> <url>`: adds the <URL> as <NAME> for the remote
- sets up the plumbing between local and remote

`git diff <FILE>`: 
- generally preferably use for individual file
- compares the latest with the state that git knows of
- alternatively can use `git diff --staged <FILE>`

`git restore <FIle>`: to restore last working version
- `git restore --staged <FILE>` to unstage
- `git restore --source <HASH>`: takes the file from point in time and copy to current state

`git restore`: will restore a previous state of your history
- can be used to unstage
- can be used to revert back to previous state
    - `git restore --source <HASH> <FILE>`

`git log`
- if the log runs off your screen, press `q`
- `git log --oneline`: show you the oneline version of `git log`

Make a change to the same file in both locations:
- `git config pull.rebase false #merge` select if asked; should have already been set up in installation
- if the changes are in separate locations of the file, first git pull from remote to merge conflicts 
- if the changes are in the same location of the file, git pull will result in automatic merge conflict, need to fix file locally first then git add, commit, and push
- `git merge --abort` to abort the merge

`.gitignore` file
- type `.ipynb_checkpoints` in the file and this checkpoint file will be ignored
- can google 'python gitignore' or 'r gitignore' for a list of common files that should be ignored
- general rule of thumb: any file that is generated over the course of projet shoudl be ignored