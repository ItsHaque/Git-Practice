## This repo contains my detailed git learning journey

## initialize a local repo
`git init`

## stage a file 
`git add <file_name>`

## Unstage a file
`git restore --staged <file>`

## stage all modified and/or new files
`git add .`

## commit changes
`git commit -m "meaningful commit message describing the changes"`

## add a remote repo
`git remote add origin <remote_link>`

## rename the local repo default branch to main
`git branch -M main`

## first push command
`git push -u origin main`

-u -> set upstream (tracking)

origin -> remote repository

main -> branch to push

## normal push from current branch
`git push`

## check remote
`git remote -v`

## add username to git which will be included in the commits
`git config --global user.name "Your Name"`

## add email
`git config --global user.email "you@example.com"`

## --global vs --local
--global to set the value for **_every repository_** on the computer.

--local (the default) to set the value only for the **_current repository_**.

## check configuration
`git config --list`

## Check File Status (tracked/ untracked)
`git status`

## View Commit History
`git log`

## Stash: saving changes without commit
 - save unfinished works (without commit) and change branch
 - useful for avoiding unnecessary commits.
 - `git stash` -> stash staged and unstaged changes (tracked only)
 - `git stash -u` -> stash untracked files as well.
 - stash stack:
   - Each time we run `git stash`, changes are saved on top of a "stack". 
   - The most recent stash is on top, and we can apply or drop stashes from the top down, or pick a specific one from the list.
 - `git stash push -m "message"` -> stash with a message.
 - `git stash list` -> list all stashes
 - `git stash show` -> show change details of the last stash
 - `git stash apply` -> restore the latest stash
 - `git stash apply 'stash@{#}'` -> restore a specific stash from the stack
 - **_applying a stash keeps it in the stack._**
 - `git stash pop` -> restore the latest stash and **_remove it from the stack_**
 - `git stash drop 'stash@{#}'` -> drop a specific stash from the stack
 - `git stash clear` -> delete the whole stash stack. **this can't be undone**
 - `git stash branch <branch_name> 'stash@{#}'` -> create a new branch from a specific stash (applying the stash in the new branch)
 - 






