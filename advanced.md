What else is possible with git?
=======================

Adding to staging
-------------
Only add already tracked files
```
git add -u
```
Follow the menu and add line by line
```
git add -i
```

Merge
-----
Merge branches into each other. Can be a fast-forward merge or a three-way merge that create a new merge commit. 
```
git merge branch
```
![](https://www.atlassian.com/wac/landing/git/tutorial/git-branches/pageSections/00/contentFullWidth/0/tabs/02/pageSections/01/contentFullWidth/02/imageBinary/git-tutorial_merge-three-way.png)

Rebase
------
Takes commits, turns them into patch files, and reapplies them on top of ontoABranchOrShaOfYourChoosing. Rewrites history.
```
git rebase ontoABranchOrShaOfYourChoosing
```

**Never rebase a shared branch!**

Rearrange, squash, rename commits
```
git rebase -i referenceBeforeTheOnesYouWantToEdit
```
![](https://www.atlassian.com/wac/landing/git/tutorial/rewriting-git-history/pageSections/00/contentFullWidth/0/tabs/01/pageSections/01/contentFullWidth/02/imageBinary/git-tutorial_rebase-merge.png)

Amend
-----
Forgot something in your last commit? 
```
git commit --amend
```
Careful, this rewrites the history, the same as rebase. 

Moving/renaming files and keeping their history
-----------
```
git mv originalFile targetFileAndLocation
git rm fileYouNoLongerWantToTrack
```

Stash
----
Stashes all your work into a temporary commit in the stash and resets your working directory.
```
git stash
git stash pop
```

Logs
----
```
git log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
# put this in your ~/.gitconfig:
# [alias]
#   hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
# --elliotc, 11/5/2015
git log --graph
git show reference
git diff reference1 reference2 -- filelist
```

Reflog
------
Git keeps track of updates to the tip of branches using a mechanism called reflog. This allows you to go back to changesets even though they are not referenced by any branch or tag. 
```
git reflog
```

References
-------
Start from your reference (branch, HEAD, ..) and go 
- '^' to the parent commit
- '^^^' or '~3' to the great-great-parent
- '^3' gets you to the third parent if you have multiple
- '^3~2^2' select the third parent, 2 down, select second parent
- '@{yesterday}' yesterdays commits
- '@{5}' this is the fifth-to-last thing that the reference pointed to, regardless of the order of commits

Tags
---
Use git tag to keep track of important commits or points of time in your repository
```
git tag nameOfTag [reference]
```

Bug-hunting
---------
```
git bisect start badReference goodReference -- files
```

Gitignore
---------
Specifies intentionally untracked files to ignore.

