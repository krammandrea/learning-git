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
```

- Discover the "bad" commit when some aspect of your code changed
```
  - git bisect start
  - git bisect good <revision1>
  - git bisect bad <revision2>
```

- View git log like a graph
```
git log --pretty=oneline -n 20 --graph --abbrev-commit

- View contributors histogram
```
git shortlog --summary --numbered


