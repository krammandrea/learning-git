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