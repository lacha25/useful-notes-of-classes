# Git

## Repository Basics

- `git init`: initialize a repository
- `git status`: inspect the working tree
- `git add`: stage changes in the index
- `git diff`: inspect changes
- `git shortlog`: list summarized commit history
- `HEAD`: the latest commit on the current branch

## Commits and History

- `git commit --amend`: add to or edit the previous commit
- `git tag -m "..."`: create an annotated tag
- `git show <id>`: inspect a commit
- `git checkout <id>`: move to an older commit
- `git rebase main`: rewrite history to make it more linear

## Branching

- `git switch -c feature/today`: create a branch and switch to it
- `git branch`: list branches and show the current branch with `*`
- `git switch main`: switch back to `main`
- `git merge feature/today`: merge a branch into the current branch

## Reset and Restore

- `git restore .`: revert tracked files to the latest committed version
- `git reset --hard <id>`: move to a specific commit and reset tracked changes
- `git reset --soft <id>`: move `HEAD` while keeping changes staged or in the working tree

## Remotes and Collaboration

- `git push -u origin <branch>`: push a branch and set upstream tracking
- A fork is your own copy of someone else's repository so you can work independently and propose changes later.
