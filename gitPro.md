The Perfect Commit
====================

1. Add the `right` changes
2. Compose a good `commit message`

> Try to consider to cover a single topic in one commit without worring about number of commits.

Add only a specific chunk of code in in a fle
=============================================
`git add -p <filepath>`

> select the **hunk** you wanna stage

The Perfect Commit Message
===========================

1. Subject = consicse summary of what happend
2. Body = more detailed explanation
    - what is now different than before
    - what's the reason for change
    - is there anything to watch out for / anything particularly remarkable


`This command will open a prompt to write detailed message`


  ``` 
  git commit
   ```

### Mesage Format

```javascript
Header

Body
     - point 1
     - point 2
// After new line, git understands that body started
```

Branching Startigies
======================
> ### A Written Convention

## Agree on a Branching Worflow in Your Team

1. Git allows you to create branches - but it doesn't tell
you how to use them!

2. You need a written best practice of how work is ideally
structured in your team - to avoid mistakes & collisions.

3. It highly depends on your team / team size, on your
project, and how you handle releases.

4. It helps to onboard new team members ("this is how
we work here").

Integrating Changes & Structuring releases
==========================================

1. ## Mainline Development
    ### "Always Be Integrating"

    - few branches
    - relatively small commits
    - high-quality testing & QA standards

2. ## State, Release, and Feature Branches

    Branches Enhance Structures & Workflows

    - different types of branches...

    - ...fulfill different types of jobs

Long-Running Branches
=====================


- exist through the complete lifetime of the project

- often, they mirror "stages" in your dev life cycle
- common convention : No direct commits

Short lived Branches
====================
- for nrw feature, bug fixes, refractoring, experiments

- will be deleted after integration (merge/rebase)

Two Exaples of Branching Startegies
==================================
 1. GitHub Flow
    - very simple,very lean : only one long running branch `main` + `feature branches`
 2. GitFlow
    - more structure
    - long running : `main` + `develop`
    - short-lived : `features` + `hotfixes` + `releases`

Pull Requests
=============
> A Pull Request invites reviewers to provide feedbck before merging

> We can contribute to other repositories without permissions by making a pull rewuest

    - fork the repository
    - change the code
    - make a pull request to integrate your  change


 Communicating About and Reviewing Code
 ======================================

**Note** : 
> Without a Pull Request you would jump right  to merging your code.., It can be done only if changes are not complicted


 Alias for git commands
 ======================

`git config --global alias.ac "!git add -A && git commit -m"`

> Now, we can use `git ac "commit message"` to add and commit our changes

`git config --global alias.ac "commit -a -m"`

> Now, we can use `git ac "commit message"` to add and commit our changes, except newly created file

Pretty Logs
============

`git reflog`

> Another simple, but useful command is reflog. This command lets you easily see the recent commits, pulls, resets, pushes, etc on your local machine. This is a great way to track down any issues that may have come up to see what you did to cause those issues

`git log --graph --decorate --oneline`

> This command combined with some special flags gives you the ability to print out a pretty log of your commits/branches.

Searching Logs
==============

`git log -S "A promise in JavaScript is very similar"`

> You can also use the log command to search for specific changes in the code. For example you can search for the text **A promise in JavaScript is very similar** as above.


Stash
======
`git stash`

> This simple command will stash all your code changes, but does not actually commit them. Instead it stores them locally on your computer inside a stash which can be accessed later. Now you can go about fixing the urgent bug and once you are done with that you can pop your changes from the stash to continue working

`git stash pop`

> This command will take all the changes from the stash and apply them to your current branch and also remove the code from the stash. This is the ideal workflow if you need to quickly stop working on your current code to start working on something more urgent.

Removing Dead Branches
======================

`git remote update --prune`

> This command will delete all the tracking information for branches that are on your local machine that are not in the remote repository, but it does not delete your local branches. In order to do that you need to run a bit of a tricky command.

`git branch -vv`

> This command will list out all of your branches and then search for any branches that have the remote tracking set to gone.

Bisect
=======
The bisect command in Git is incredible for finding which commits caused certain bugs. It is very common for a repository to have thousands of commits from hundreds of developers so when a bug report comes in it can be tricky to track down which changes caused this issue. With bisect, though, this problem is trivial. In order to understand why this command is so amazing let’s look at how to use it.

```javascript
    git bisect start
    git bisect bad
    git bisect good 48c86d6
```
To start a bisect you need to run three commands. The first command starts the bisect. The second command tells Git which commit is the bad commit with the bug. If you leave this blank, as we have, Git will just use the latest commit. The final command tells Git which commit is known to not have this bug. In our example we know that in commit 48c86d6 there is no bug.

Now after you run these three commands Git will choose the commit in the middle of these two commits and grab all the code from that commit. You can then test to see if the bug is in this commit or not. If the bug is present you just type git bisect bad and it will select the commit that is halfway between this bad commit and the last good commit. If the bug is not present then you can type git bisect good and Git will select the commit that is halfway between this good commit and the last bad commit. You keep repeating this process of typing either good or bad until eventually you are able to narrow it down to the exact commit that caused the bug.

This is amazing at narrowing down your bug search since some bugs can be really hard to track down without knowing what code was changed to cause it.

Destroy Local Changes
=====================
`git reset hard origin/main`

The above command says to forcefully delete all local changes on your current branch and replace them with the code from the main branch in the remote.

> It is important to note that this will remove all local changes you have made so only do this if you really want to delete all the changes you have made and need to start fresh.



