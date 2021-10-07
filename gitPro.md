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


## Communicating About and Reviewing Code

**Note** : 
> Without a Pull Request you would jump right  to merging your code.., It can be done only if changes are not complicted
