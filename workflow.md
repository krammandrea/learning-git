Team workflow  
============

Get your own branch started
---------
```
git checkout master
git pull
git branch yourName/pickANameForYourChanges
git checkout yourName/pickANameForYourChanges
```

Commit a change  
---------
```
git status     
git diff    #shows your changes line by line
git add pathNameToFile
    # or 
git add -u  #all the files you have changed
git commit -m "commitMessage"
```

Save remotely
------------
```
# set up the remote target once
git branch --set-upstream yourName/pickANameForYourChanges origin/yourName/pickANameForYourChanges 
git push
```

Deploy to staging
---------
before pushing to staging, update from master again
```
git checkout master
git pull
git checkout yourName/pickANameForYourChanges
git rebase master
git status    To check if there was a conflict
git push -f origin yourName/pickANameForYourChanges
git push -f origin yourName/pickANameForYourChanges:staging
```
- Check if build was successful on Jenkins
- Review your work

Review
-------
- Go to the repositories github page
- Create a pull request from your branch
- Alert team members to review the pull request and what you pushed to staging

Deploy to production
---------
- Repeat staging step if anything changed on master in the meantime
- Use the merge button in the pull request to merge to master
- Start Build Now on Jenkins 
