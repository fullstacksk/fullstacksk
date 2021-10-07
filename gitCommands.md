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

