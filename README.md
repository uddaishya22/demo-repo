## Undoing (branch: undoing)
### reset before commiting after adding:
### -> undo staging
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


### undo commits
