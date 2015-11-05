Status
-----
Check on your status. It shows your 
- Current branch
- Changes to be committed
- Changes not staged for commit
- Untracked files
- Instructions on how to get from one area to another
```
git status
```

Branches
-------
Branches are used to develop features isolated from each other. The master branch is the "default" branch when you create a repository. Use other branches for development and merge them back to the master branch upon completion.

Create branch and switch into with 
```
git checkout -b your_name/pick_a_name_for_your_changes
```
Switch branches with 
```
git checkout branchName
```
![](https://www.atlassian.com/pt/git/workflows/pageSections/00/contentFullWidth/0/tabs/01/pageSections/07/contentFullWidth/0/content_files/file0/document/git-workflow-feature-branch-1.png)


Staging Area / Index
-----------
The staging area is an assembly point of files you want to commit. You can stage some files, even parts of files, to be committed, while leaving other changes for later commits.
```
git add fileName
```
See line by line changes you're about to commit
```
git diff --staged
```

Commit
------
Keep related changes together in separate commits
To commit everything from the staging area to HEAD
```
git commit -m "The commit message"
```

Pulling from remote
-----------------
Merge upstream changes into your local repository
```
git pull --rebase
```
![](https://www.atlassian.com/pt/git/workflows/pageSections/00/contentFullWidth/0/tabs/00/pageSections/05/contentFullWidth/00/content_files/file1/document/git-workflow-svn-6.png)

Pushing to remote
---------
To send changes to remote repository, set up the remote target once
```
git branch --set-upstream your_name/pick_a_name_for_your_changes origin/your_name/pick_a_name_for_your_changes 
```
```
git push
```
![](https://www.atlassian.com/wac/landing/git/tutorial/remote-repositories/pageSections/00/contentFullWidth/0/tabs/03/pageSections/01/contentFullWidth/00/imageBinary/git-tutorial_repos-push.png)

**Never force push to a shared branch!**

Merge conflict
----------
Uh oh, I rebased or merged and there is a CONFLICT
- `git status`
- Find the files in the Unmerged paths and open them 
- Search for '<<<<<<' that indicate the conflicting lines
- Construct appropriate resolution
- Remove all lines with '<<<<<<', '=======' and '>>>>>>>'
- Save the file 
- Follow instructions on git status

OR 
- Nevermind, abort please
```
git merge --abort
```

Logs
----
- Use a client or
- `git log --graph --oneline --decorate --all`

Introduction to vi-commands
--------------
- 'esc' for command modus
- 'i' for insert modus
- 'esc' + 'dd' + 'p' to delete one line and paste it again
- 'esc' + ':wq' to save file and exit vi


