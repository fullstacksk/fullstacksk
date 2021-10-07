Createing a repository
========================
`…or create a new repository on the command line`

```javascript
echo "# fullstacksk" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:fullstacksk/fullstacksk.git
git push -u origin main
```

`
…or push an existing repository from the command line
`

```javascript
git remote add origin git@github.com:fullstacksk/fullstacksk.git
git branch -M main
git push -u origin main
```

`...Or else You can initialize this repository with code from a Subversion, Mercurial, or TFS project.`
See the changes
===================================
`git status`

See changes within a file
===================================
`git diff <filePath>`

Add particular file to staged area
===================================
`git add <filePath>`

Add all files to staged area
=============================

`git add .`

Add only a specific chunk of code in in a fle
=============================================
`git add -p <filepath>`

> select the chunk you wanna stage


Commit the changes
===================================
`git commit -m "<message>"`

Push the changes to remote first time
===================================
`git push -u <remote_name> <branch_name>`


Push the changes
===================================
`git push`

Push a new branch 
===================================
`git push --set-upstream <remote_name> <branch_name>`

Merge a branch
===================================
`git merge <branch_to_be_merged>`


UNDO Merging
===================================
`git merge --abort`

> It is helpful when we got complex conflicts.


Rebase a branch
===================================
`git rebase <branch_to_be_merged>`


UNDO Rebasing
===================================
`git rebase --abort`

> It is helpful when we got complex conflicts.

Merge Vs Rebase
================
    - Rebase preserves original commit structure while merging we have to do merge commit
    - Rebase rewrites commit history

Warning Notice
===============

1. `Do NOT use Rebase on commits that you've already pushed/shared on a remote repository!`

2. `Instead, use it for cleaning up your local commit history before merging it into a shared team branch.`