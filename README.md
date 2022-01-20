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

