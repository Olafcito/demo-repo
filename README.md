# Installation
https://www.atlassian.com/git/tutorials/install-git 
- For Mac homebrew is recommended 
- I believe BASH is recommended for Windows
# Commands
![image](https://github.com/Olafcito/demo-repo/assets/122600472/03b7e91e-1feb-45ba-8eb0-9e2fea7327e5)

## Commands (for windows Git Bash is recommended)

- cd ~/OneDrive/Dokumenter/Python\ Projekter/Git\ tutorial/demo-repo
    - Navigates to branch "~/OneDrive/Dokumenter/Python Projekter/Git tutorial/demo-repo", backslash displays how to handle spaces
- git status (shows all the files that were updated or deleted, but havent been saved in a commit yet)
- git add . - adds all files or -add <file>
        - Untracked files havent been added to git yet, so we need to use git 
- git commit -m "Title of the message to be added" -m "The description box"
    - saves code locally, isnt live on Github yet
- git push 
    - pushes live to remote repository

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

## See ChatGPT for transfer to macbook

### Public SSH key
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJBvKWyiB+GNbFuyyG6xYb1fIe7LF3Tel08nTppb9fGq solarsen12@gmail.com
### Private SSH key
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACCQbylsogfhjWxbsshusWG9XyHuyxd03pdPJ06aW/XxqgAAAJgIq9ReCKvU
XgAAAAtzc2gtZWQyNTUxOQAAACCQbylsogfhjWxbsshusWG9XyHuyxd03pdPJ06aW/Xxqg
AAAEDK/Y5dAFYqfhwHmYc2KBx8w06107uCRWjzVXCi+IPyiJBvKWyiB+GNbFuyyG6xYb1f
Ie7LF3Tel08nTppb9fGqAAAAFHNvbGFyc2VuMTJAZ21haWwuY29tAQ==
-----END OPENSSH PRIVATE KEY-----