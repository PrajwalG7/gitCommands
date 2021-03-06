# git commands:

# 1 git config

A) To config your user.name and user.email:

- git config --global user.name "Your name"
- git config --global user.email "your email"

B) To see the changes made in config:

- git config --global user.name
- git config --global user.email

C) To edit the config:

- git config --global --edit

# 2 Creating a Git Repository

1. To make a new directory:

- mkdir <directory name>

2. To make that directory your repo :

- git init

3. To see current the current directory contents:

- ls

4. To see .git file (it will tell which files are tracked by git):

- ls -a

5. To see what changes are made in the repo (repository):

- git status

# 3 Git Staging area

We track the file and then we commit.
To do so...

1. To track the file or to add the file in staging area:

- git add <file name>
  or
- git add .

Flow: working directory -> git add -> staging area -> git commit -> repository

2. To commit the file:

- git commit -m "message of commit"

3. To see previous commits:

- git log

# 4 Git checkout

1. The git checkout command is used to switch between branches in a repository or the commits:

- git checkout <commit hashcode/branch name>

2. To get back:

- git checkout master

# 5 Git branch

1. To see the branch:

- git branch

2 To create a branch:

- git branch <branch name>

3. To create a branch and checkout at same time with single command:

- git checkout -b <branch name>

# 6 git merge

Lets say we have created a new branch named "dev" and again we have created an another branch name "Newfeature" so now we have to merge that NewFeature branch to the dev branch so we use:

- git merge <branch name>

Now lets say we have merged NewFeature with dev now we have to merger the dev branch to the master branch so we again use:

- git merge <branch name>

# 7 .gitignore

So what if we want some files to not to be tracked by git so we add that files to git ignore file

1. create git ignore file:

- touch .gitignore
  then add the files in .gitignore
  Even we can add .gitignore file to .gitignore

# 8 Creating a GitHub repo

Go to github and create a new repo now thats the remote
we have to add the local changes to remote so we use git push
The steps are:

- git remote add origin <repoLink>
- git branch -M master
- git push -u origin master

Explanation:
Here git remote add origin <repoLink> means to a add a new remote,

- git branch -M master means move master branch to remote,
- git push -u origin master this will push your code to the master branch of the remote repository defined with origin and -u let you point your current local branch to the remote master branch

# 9 To clone a repo

Go to the repo and clone the url
(Clone in another folder)

- git clone <repo url>

To see the changes made in specific file:

- cat <file name>

Now as you have made changes and if you want to update your codebase first you need to add files in staging area then commit it with a message and push to the origin.

---

# Open source Contribution basics:

- Step 1: fork a repo to which you want to contribute to.
- Step 2: Clone the repo.
- Step 3: make changes into files.
- Step 4: to update the codebase add the files in staging area, commit the files with short desc of changes, push the file to your remote.
- Step 5: Go to contribute in your remote repo and click open pull request
- Step 6: Review your changes.
- Step 7: Click create pull request and write what changes you have made in messagebox and again click create pull request.
  Now you have successfully created your first PR (pull request).

Now the owner of the original repo will receive that pull request and in under Pull request section he/she/team will check the changes made by your side under file section, they will review your changes by "Review changes" option which has 3 SubOptions:

1. Comment
2. Approve
3. Request changes, and if they found the changes are valid then they'll approve and merge your PR.
