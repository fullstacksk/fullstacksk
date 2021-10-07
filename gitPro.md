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