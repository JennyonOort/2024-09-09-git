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