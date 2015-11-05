Tips and Tricks
===============

- Color is easier to read
```
git config color.ui true
```

- All your branches and SHAs. In one line. With colors.
```
git log --graph --oneline --decorate --all
```

- Use git bisect as the repair tool of last resort...when things really go wrong
```
git bisect start
git bisect good  //this commit does not exhibit the issue
git bisect bad   //this commit exhibits the issue
```

- I messed up stuff on my local, reset to what's on origin
```
git fetch origin
git reset --hard origin/branchYouWantToResetTo
```

- I have to get that commit on top of something without a rebase
```
git checkout targetBranch
git cherry-pick commitSHA 
```

- Git Tools - Stashing
```
git stash
git stash list
git stash apply
```
https://git-scm.com/book/en/v1/Git-Tools-Stashing

- How many lines have changed in each file
```
git log --stat
```

- Who wrote this wonderful line of code?
```
git blame -M -C -C
```

- I wanted to start a new branch 3 commits ago
```
git branch newBranchName referenceOf3CommitsAgo
```

- I'm working on a fork, and want to merge in changes from the original repo.
```
git remote add upstream {Public Clone URL}
git pull upstream master
```

- I want to clean untracked files
```
git clean
```
