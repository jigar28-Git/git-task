# Git Basic Task ![github_git_icon_145985](https://user-images.githubusercontent.com/119313004/216284173-4b43f453-e99a-4ad6-b444-247243dcf2bb.png)


### Create Repository :
- A new repository can either be created locally, or an existing repository can be cloned. When a repository was initialized locally, you have to push it to GitHub afterwards.
```
$ git init
```
- The git init command turns an existing directory into a new Git repository inside the folder you are running this command. After using the 
``` git init ``` command, link the local repository to an empty GitHub repository using the following command:
``` 
$ git remote add origin [url] 
```
- Specifies the remote repository for your local repository. The url points to a repository on GitHub.
``` 
$ git clone [url]
```
- Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits

### Configure tooling :
- Configure user information for all local repositories
```
$ git config --global user.name "[name]"
```
- Sets the name you want attached to your commit transactions
```
$ git config --global user.email "[email address]"
```
- Sets the email you want attached to your commit transactions
```
$ git config --global color.ui auto
```
- Enables helpful colorization of command line output.

# Practical Task ![git_logo_icon_145254](https://user-images.githubusercontent.com/119313004/216284555-5a55fa67-7eb1-4ce4-8e40-48876408a9ef.png)


## #1 Pull-Request and Merge :
- **1. Switch to the branch that you want to create a pull request for.**
```
$ git checkout ＜branchname＞
$ git push -u origin compair_branch_name
```
- **2. Click Create Pull Request. GitHub Desktop will open your default browser to take you to GitHub.**

 ![create pull request](https://user-images.githubusercontent.com/119313004/216275646-718cf67c-36d0-40e9-9e67-a5c25413bbdb.png)

- **3. Type a title and More About Your Pull-Request for your pull request.**

![add contribute](https://user-images.githubusercontent.com/119313004/216276731-8c0e426c-73b9-4ede-8830-ea1e098d0947.png)

-  **4. To create a pull request that is ready for review, click Create Pull Request, use the drop-down and select Create Pull Request, then click Pull Request.**

![creatpullreqopt](https://user-images.githubusercontent.com/119313004/216278649-d5a1fe67-8a5d-459d-8548-3752730ce2a2.png)

## #2 Git Rebase :
- Rebase is one of two Git utilities designed to integrate changes from one branch onto another. Rebasing is the process of combining or moving a sequence of commits on top of a new base commit. Git rebase is the linear process of merging.

![rebase](https://user-images.githubusercontent.com/119313004/216287695-df675156-fa85-4bc8-99ae-739c4b2da886.png)

#### What rebase do :
- Reverts all commits since the current branch diverged from upstream branch, and then re-applies them one-by-one on top of changes from the HEAD of upstream branch.
#### command :
```
$ git rebase "branch_name"
```

## #3 Change commit message :
- If the commit only exists in your local repository and has not been pushed to GitHub.com, you can amend the commit message with the ```$ git commit --amend``` command.
#### Steps :
**1. If the commit only exists in your local repository and has not been pushed to GitHub.com, you can amend the commit message with the git commit --amend command.**

**2. Type  ``` git commit --amend ``` and press Enter.**

**3. To change recent Commit and add the Message you can also write belowed code**
```
git commit --amend -m "New commit message"
```
> What the command does is overwriting the most recent commit with the new one.

**3. If you completely changed the commit message than you can push commit to the branch.**


## #4 Cherry pick commit :
- To demonstrate how to use git cherry-pick let us assume we have a repository with the following branch state :
```
 a - b - c - d   Main
       \
        e - f - g Feature
```
- ```git cherry-pick``` usage is straight forward and can be executed like :
```
 git cherry-pick commit
```
- In this example commitSha is a ***commit*** reference. You can find a commit reference by using ***git log***. In this example we have constructed lets say we wanted to use commit `f` in ***main***. First we ensure that we are working on the main branch.
```
git checkout main
```
- Then we execute the cherry-pick with the following command:
```
git cherry-pick f
```
- Once executed our Git history will look like:
```
    a - b - c - d - f   Main
         \
           e - f - g Feature
```
- The `f` commit has been successfully picked into the main branch
## #5 Drop Commit Message :
- Generally, the ```git reset``` command is used for deleting the latest commits in Git, To delete the most recent commit, run the command below :
```
git reset --hard HEAD~1
```
- To delete the N-th latest commits, you should use HEAD~N as the argument of git reset.
```
git reset --hard HEAD~N
```
- As an alternative to this method, you can select the appropriate commit by its hash instead of HEAD~N, Here is how to do it :
```
git reset --hard <sha1-commit-hash>
```
# To Fetch remotely created folders in to main branch :
- ***commands :***
```
git fetch --all
```
> to fetch the all folders
```
git checkout main-copy
```
> This will make copy of the main branch. 
```
$ git checkout - 
```
> To go to the main branch or previous branch.
```
$ git reset --hard origin/main  
```
> This will push the all folders that you are created remotlly.

### Result Demo :

|   Before    |   After    |
| :-----------: | :-----------: |
|![Screenshot from 2023-02-03 11-56-52](https://user-images.githubusercontent.com/119313004/216529621-8fd0b6a2-cedc-4214-ac53-545145b4d7dc.png) | ![Screenshot from 2023-02-03 11-56-44](https://user-images.githubusercontent.com/119313004/216529636-6e807ff4-dd48-4a02-aa92-f2221bb00488.png) |
