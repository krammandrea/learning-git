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

- Autocomplete for zsh

Just get [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh) and add the git plugin to
your zshrc:

```
# find this line add add git if it's not there yet
plugins=(git osx)
```
