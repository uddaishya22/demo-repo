## Undoing (branch: undoing)
### reset before commiting after adding:
### -> undo staging
>git reset <arguement>
If we added the file and not commited yet, then we can use command 'reset':
for eg:
> git add <file_name>
> git status
> git reset 
we will get:
    Unstaged changes after reset:
    M       README.md

check the status again:
> git status

we will get:
    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")


### undo just made commit: git reset HEAD~<pointer>
To go back to the commits lets say we wanna go back 2 or 3 commits back then we can use HEAD pointer with reset
if we want to go back to the previous commit :
>git reset HEAD~1

['HEAD' is a pointer]

### undo commits by their hashing:
1. To get back a particular commit we have to copy that commit hashing either from log in local or from github.
> git reset <commit_hashing>

for example:
> git reset 91bac69d261fec103f84b99b666cfe28f1f20489

we will get:
    Unstaged changes after reset:
    M       README.md

2. In the previous case we will be on an unstaged situation but if we want to remove all of those changes and want to revert as it was in the commit then we will be using '--hard' before commit hashing.

> git reset ---hard <commit_hash>