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
git branch newBranchName HEAD~3
```

or

```
git branch newBranchName HEAD^^^
```

- I'm working on a fork, and want to merge in changes from the original repo.
```
git remote add upstream {Public Clone URL}
git pull upstream master
```

- Make `git pull --rebase` the default mode.

On `~/.gitconfig`, add this:

```
[push]
        default = simple
```

or use git to set the preference:

```
git config --global push.default simple
```

- Force-pushing to staging ;-)
```
git push -f origin HEAD:staging
```

- Have a bug? Don't know which commit introduced that bug? Do a git bisect!!! This uses binary search to find the commit that introduced a bug.
```
git bisect start
git bisect bad                 # Current version is bad
git bisect good v2.6.13-rc2    # v2.6.13-rc2 is known to be good
```

- I want to clean untracked files
```
git clean
```

- I'm working on a fork, and want to merge in changes from the original repo.
```
git remote add upstream {Public Clone URL}
git pull upstream master
```

- Have a bug? Don't know which commit introduced that bug? Do a git bisect!!! This uses binary search to find the commit that introduced a bug.
```
git bisect start
git bisect bad                 # Current version is bad
git bisect good v2.6.13-rc2    # v2.6.13-rc2 is known to be good
```
