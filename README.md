# Installation
https://www.atlassian.com/git/tutorials/install-git 
- For Mac homebrew is recommended 
- I believe BASH is recommended for Windows
# Commands
![image](https://github.com/Olafcito/demo-repo/assets/122600472/03b7e91e-1feb-45ba-8eb0-9e2fea7327e5)

## Initialize new repo locally
- git init
    - "Initialized empty Git repository in C:/Users/Olaf Larsen/OneDrive/Dokumenter/Python Projekter/Git tutorial/demo-repo-locally-created/.git/" 
- Create empty repo at Github.com
    - Copy SSH key
- git remote add origin git@github.com:Olafcito/emptyrepo.git
    - remote: somewhere else but not on this computer
- git remote -v
    - shows any remote repository connected to this repo
- git push -u origin master 
    - u: sets upstream so origin master doesnt need to be typed
## Commands in repo (for windows Git Bash is recommended)
- git remote -v
    - shows content of repository, useful to see what repo you currently are in
- cd ~/OneDrive/Dokumenter/Python\ Projekter/Git\ tutorial/demo-repo
    - Navigates to branch "~/OneDrive/Dokumenter/Python Projekter/Git tutorial/demo-repo", backslash displays how to handle spaces
- git status (shows all the files that were updated or deleted, but havent been saved in a commit yet)
- git add . - adds all files or -add <file>
        - Stages changes 
        - Untracked files havent been added to git yet, so we need to use git 
- git commit -m "Title of the message to be added" -m "The description box"
    - saves code locally, isnt live on Github yet
    - no message will be returned
    - Type ":q!" to escape in general
- git push origin master | git push origin main
    - origin: std. location of Git repository
    - master: branch we want to push to 

### Commands in branch
- git branch
    - shows which branch you are in 
- git branch
    - useful for displaying branch
- git checkout <name>
    - switch between branches
    - git checkout -b <name> adds a new branch
- git diff <other branch>
    - See other code merging in
- git push
    - Pushes it up to branch, copy paste:
    - git push --set-upstream origin <branch-name>
#### Merging branches requests
- push changes to branch
- Either you can
    - git merge <other branch> (from main)
        - merges files and directly commits to merge
    - push as seperate as branch, go to Github.com --> make pull request --> review --> merge

# Connect device to Github commands
## Connect machine to Github commands with SSH
- creating a github key
    - ssh-keygen -t ed25519 -C "solarsen12@gmail.com"
        - Just pick default location/key
        - passphrase can be left blank 
- Following commands
    - eval $(ssh-agent)
    - ssh-add ~/.ssh/id_ed25519
    - cat ~/.ssh/id_ed25519.pub
        - Outputs public key

## Verify that local Git client is configured with SSH key
- ssh -T git@github.com
- Should output Warning: Permanently added the ED25519 host key for IP address '140.82.121.4' to the list of known hosts. Hi Olafcito! You've successfully authenticated, but GitHub does not provide shell access. 
