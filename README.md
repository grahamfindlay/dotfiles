Perform all steps in order. 

### Install Git ###

### Install Oh-My-Zsh ###
```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Install tmux ###
```
brew install tmux
```

### Install MacVim (mvim) ###
```
brew install macvim --with-override-system-vim
brew linkapps macvim
```
Confirm success with:
```
ls -la `which vim`
```
You should see it symlinked to the macvim Cellar. 


