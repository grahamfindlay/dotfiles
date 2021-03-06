# About these dotfiles
The Cardinal Rule of this Branch: **Not a single line goes into any of these dotfiles that you don't understand completely.**

The primary goal of these dotfiles is portability. That means a setup that "just works". And one that you can debug if needed. Try not to require anything that doesn't ship with the latest Ubuntu LTS release. Shoot for less than 5 minutes from the time of cloning until you're in business, guaranteed. You can get fancy and add the optional extras on your own machine. 

# Install
Perform all steps in order: 

1. Install Git
2. Clone this repo.
  * Use `git clone --recursive` to pull all submodules, or `git submodule update --init --recursive`` if you've already cloned. 
3. Install Oh-My-Zsh (*Optional, but highly encouraged*) 
  * `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
4. Install dotfiles
 * You can use either the rakefile or the bash script `bootstrap` to symlink files. 
   Both scripts will give you the option to backup any files they try to clobber 
    ```
    cd path/to/this/repo
    rake install
    ```
    or
    ```
    cd path/to/this/repo
    bash bootstrap
    ```

# Optional extras
Now, if you have time:

1. Install a version of vim that was compiled with the +clipboard option, so that you can copy-paste to the system clipboard. 
  * `sudo apt-get install vim-gnome` if you're not installing YouCompleteMe or are using Debian 9. If installing YouCompleteMe on Debian 8, you probably have to build vim from source. Instructions [here](https://github.com/Valloric/YouCompleteMe). You may have to set --enable-gui to gnome2 rather than gtk2 when using Debian 8.
2. Customize Terminal
  * Install Solarized Colors for Terminal. 
3. Install GNOME Tweak Tool
  * `sudo apt-get install gnome-tweak-tool`
  * Remaps Caps Lock to Ctrl
4. Install Ag
  * `sudo apt-get install silversearcher-ag`
  * If you have trouble installing Ag...
5. Install [YouCompleteMe](https://github.com/Valloric/YouCompleteMe)
  * Rather than using Vundle, you can use Pathogen. 
  ```
  cd ~/.vim/bundle
  git clone https://github.com/Valloric/YouCompleteMe.git
  cd YouCompleteMe
  git submodule update --init --recursive
  ./install.sh --clang-completer
  ```  
  Done!
