# Git workflow
Workflow guide for the Stikky Dev Team when it comes to Git & Collaboration

# Summary
Git can appear overly complex to use at first glance, but with a little practice it is the single most powerful tool a team can use for collaboration when working on project.

# Setup
## Installation
- Windows 10: Head to [Git for Windows](https://gitforwindows.org/) and install (ignore the GUI application this also installs we are going to use the command-line to operate git). Check installation worked once it's finished with the following command.
```
git --version
```

## Set up GitHub account with your local Git Install
```
git config --global user.name "your-github-username"
```

```
git config --global user.email “you@example.com”
```
## SSH Key
### We now need to generate an SSH key which allows you to clone, pull and push to GitHub without entering your password every time.
```
ssh-keygen
```
- Press enter when asked where to save it, press enter again to overwrite if prompted
- Press enter when asked to create a passphrase, we will leave this blank
- CD into the folder that contains your new SSH key
- This key is usually saved in C:/Users/[your-windows-username]/.ssh/
```
cat id_rsa.pub
```
- Copy the full text this command shows in the terminal
### Github Account Settings
- Head to SSH and GPG keys in your account and click 'New SSH Key'
- Paste the key you just copied from your terminal
- Give it a name so you know which computer it is
- You can now use your GitHub account on your computer without needing to type in a password

# WSL
Windows Subsystem for Linux is a Windows Application installed from the Microsoft store which allows you to run a virtualized headless Linux installation on your Windows PC without a bunch of extra software or configuration. You will need a PC that supports CPU level virtualization. In short, after you install WSL you will have a Linux terminal you can open just like the Windows command prompt and run any Linux terminal applications or use it for development.

# NVM
### Note: NVM is for MacOS & Linux shell, there is a fork that is a windows version but I haven't used it
[NVM](https://github.com/nvm-sh/nvm) version manager for NodeJS and NPM that let's you install many versions of NodeJS on your system and quickly pick which to use for best compatibility with a project.
## Install NVM
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
# Common Git lingo and what they mean
- Repo/repository: The folder of all the files, the 'remote' repo is the version stored on GitHub and the 'local' version is the one you've downloaded to you computer
- Commit: Every so often when you make a change to a file, you make a commit, what this does is lets you write a short message on what you did and provides a spot you can roll the file back to if you break things. Usually commits are done as frequently as is reasonably possible, every time you successfully write a chunk of code.
- Pull: This is when you download the latest version of the repo from the remote server and update your local version
- Push: This is when you upload your changes to the remote server and update it with the new code you've written. Usually done after each commit
- Branch: A git repo has branches, which allows you to create a parallel version where you can add new features, changes, which won't affect the master branch/working version of your code
- Merge: Once features or changes are successfully done on a branch, you merge the branch in to your master branch, which will automatically merge your changes into your main working branch (when done properly)
- Pull Request: Once you finish work on your branch, your feature is working, and you've pushed your code to github, you create a pull request on github. This is just a fancy way of saying you've sent a request to the main dev to merge your branch with the main branch. The main dev can review the changes, and if everything was done properly they can merge the branch in to the main branch automatically without doing any additional work.

# Merge Conflicts and how to avoid them
- Merge conflicts can significantly slow the process and can be 100% avoided if the team works together properly
- A merge conflict happens when two different people edit the same file or lines of code, then Github gets confused on which lines it's supposed to use to overwrite the old version of the file -- Single Point of Truth is the key phrase here
- All we have to do to avoid this is to communicate which files each person is in charge of/working. To help this, projects are typically broken down in to lots of seperate files, that way each person works in their own file
- Typically once the work is finished, everyone stops working on their files and one person takes the functionality created from them and integrates them into the main larger project files, not by copy and pasteing but importing them etc.

# Commiting workflow
- Doing commits is actually a simple process to follow and helps out a ton



# Different aspects we will cover
- Creating a new repository
- Cloning an existing repository to your computer
- Commiting code and pushing it to a repository
- How to write proper commits
- Using Git with VSCode
- What a .gitignore does
- How to collaborate with a team on a project
- What branches are and how to use them
- Importance of secrets and using environment variables
- Order of operations and keeping everyones code in sync
- Pull requests and how they work
- Merge conflicts and what to do to avoid them
- General rules to make life with Git easier and more enjoyable for everyone

# If we have extra time
- WSL
- NodeJS
- NVM
- NPM Packages
- Package.json
- Package-lock.json
- NPM commands
- Project file structures






