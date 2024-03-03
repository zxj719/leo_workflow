# leo_workflow
Records of my work in Ubuntu for leo rover development.

## 1. How to use github
### Following steps will only happen once for setting up.
Install git
```bash
sudo apt install git
```
Set your profile first, take mine for example
```bash
git config --global user.email "xingjian_zhang719@outlook.com"
git config --global user.name "ZXJ"
```
Connect your computer with your github with SSH. We have to generate a pair of keys. private one and public one
```bash
ssh-keygen -t rsa
```
After three times pressing Enter, then, open and copy the public one
```bash
vim ~/.ssh/id_rsa.pub
```
Open your github website(make sure you have signed up), click the right top button and find the "settings", and find an entry to new a SSH key(I'm sure you are clever enough to find  it), paste your public key in the Key area. Don't forget to save! You can always check it using the command(along with a 'yes', perhaps)
```bash
ssh -T git@github.com
```

### And the followings may happen all the day.
Now, git your local repository. In your target directory, which the one you want to upload to the github,
```bash
git init
```
you can add them all to staged status ones
```bash
git add .
```
or you can designate several of them
```bash
git add <file name>
```
then turn them into unmodified status
```bash
git commit -m "blablabla"
```
connect your local repository with your github repository(that you have created), copy the SSH key by choosing the "SSH" in your github repository "Code" options(that green button naming "Code", yes, click it)
```bash
git remote add origin <your just copied ssh key>
```
Now, we can upload, or 'push' our local files
```bash
git push -u origin master
```
Now you can find your files in your github project 'master' branch.

Also, you can remove the origin SSH connection so that you can conncet to another remote repo.
```bash
git remote remove origin
```
In order to avoid conflict or update our version, create a new branch
```bash
git branch <branch name>
```
and you can switch to that one by
```bash
git checkout <branch name>
```
suddenly you want to remove it
```bash
git branch -D
```
to check the branch you can
```bash
git branch
```
to check the current branch status
```bash
git status
```
to check the log
```bash
git log
```
