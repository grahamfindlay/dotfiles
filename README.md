# About these dottiles
The Cardinal Rule of this Branch: **Not a single line goes into any of these dotfiles that you don't understand completely.**

The primary goal of these dotfiles is portability. That means a setup that "just works". And one that you can debug if needed. Try not to require anything that doesn't ship with OS X. Shoot for less than 5 minutes from the time of cloning until you're in business, guaranteed. You can get fancy and add the optional extras on your own machine. 

# Install
Perform all steps in order: 
1. Install Git
  1. Clone this repo.
2. Install iTerm2
  1. You want a monospaced, sans font. Use Monaco by default. 
3. Install Homebrew
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
4. Install Oh-My-Zsh (*Optional, but highly encouraged*) 
```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
5. Brew tmux
6. Brew MacVim (mvim)
```
brew install macvim --with-override-system-vim
brew linkapps macvim
```
Confirm success with: ``ls -la `which vim```
`
You should see it symlinked to the macvim Cellar. 
7. Install dotfiles
```
cd path/to/this/repo
rake install
```
The install script will give you the option to backup any files it tries to clobber. 

# Optional extras
Now, if you have time:
1. Customize iTerm
  1. If you want to get fancy, go for DejaVu Sans mono or Inconsolata. 
  2. Preferences -> Keys -> set `option-t` to show/hide iTerm 
  3. Install Solarized Colors for iTerm 2. 
2. Install Seil
  1. Remaps Caps Lock to Escape (or Ctrl)
3. Install Slate
4. Install Ag
```
brew install the_silver_searcher

```
If you have trouble installing Ag...
```
brew uninstall pcre && brew install pcre
brew uninstall --force xz && brew install xz
sudo chmod -R 777 some/problem/dirs
brew link --overwrite xz
brew install the_silver_searcher
ag searchtext path/to/code
```
