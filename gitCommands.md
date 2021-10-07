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

Add particular file to staged
===============================
`git add <filePath>`

Add all files to staged
========================

`git add .`


