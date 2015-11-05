Scripts
=======

- Autocomplete
``` 
curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash
```
Add following lines to your bash profile
```
if [ -f ~/.git-completion.bash ]; then
  . ~/.git-completion.bash
fi
```
