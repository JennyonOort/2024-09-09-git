# 2024-09-09-git 

# git add . => add all files in the current working directory; best practice is always to check the appropriate files has been added with git status

`git remote add <NAME> <url>`: adds the <URL> as <NAME> for the remote
- sets up the plumbing between local and remote

`git diff <FILE>`: 
- generally preferably use for individual file
- compares the latest with the state that git knows of
- alternatively can use `git diff --staged <FILE>`

`git restore <FIle>`: to restore last working version
- `git restore --staged <FILE>` to unstage
- `git restore --source <commit source code>`: takes the file from point in time and copy to current state

`git restore`: will restore a previous state of your history
- can be used to unstage
- can be used to revert back to previous state
    - `git restore --source <HASH> <FILE>`
- if the log runs off your screen, press `q`