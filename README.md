# dotfiles
Sunny's MacOS Dotfiles

Follow the steps for Sunny's ideal dev set up. 

## Basic Installations

1. Install iTerm
2. Install Homebrew: https://brew.sh/
3. Install git: `brew install git`
4. Configure git:
    `git config --global user.name "FirstName LastName"`
    `git config --global user.email "email@domain.com"`
5. Check configuration
    `git config --global user.name`
    `git config --global user.email`
6. Install text editor of choice: 
    `brew tap caskroom/cask`
    `brew cask install visual-studio-code`
7. Configure text editor as default editor for git:
    `git config --global core.editor "code --wait"`
    `git config --global -e`
8. Use previous command to add following lines to git config:
    '''[diff]
    tool = default-difftool
    [difftool "default-difftool"]
    cmd = code --wait --diff $LOCAL $REMOTE'''

## Zsh Glow Up

1. Install zsh: `brew install zsh`
2. Install Oh My Zsh: `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
3. Copy repo's `.zshrc` file and paste into local `~/.zhsrc` file
4. Ensure `export=` and `source` zsh directories are accurate with macname+files
5. Install Powerline9k themes for Oh My Zsh: `git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k`
6. Install Powerline9K fonts for more selection:
```
    # clone
    git clone https://github.com/powerline/fonts.git --depth=1
    # install
    cd fonts
    ./install.sh
    # clean-up a bit
    cd ..
    rm -rf fonts
```
7. Install Homebrew fonts for icons: 
    `brew tap caskroom/fonts`
    `brew cask install font-hack-nerd-font`
8. Open iTerm Preferences `CMD + ,` > Profiles > Colors
9. Load `Dracula.iterm` in Color Presets at the bottom right, then select it from drop down
10. Go to Text tab Change Font to `Droid Sans Mono for Powerline` and change font size to 14
11. Check off `Use a different font for non-ASCII text` and select either `Droid Sans` or `Hack Nerd Font` and change size to 14
12. Set up syntax highlighting: `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
13. Ensure all plugins are activated in `plugins=( [plugins...] zsh-syntax-highlighting)`

## Spotify-Terminal Glow Up

1. Install Spotify for Mac 
2. See if iTerm recognizes active songs from Spotify, if not: `brew install shpotify`
3. Create a Spotify for Developer App from spotify's website: https://developer.spotify.com/dashboard/applications
4. Add Client ID and Secret key in config file using: `code ${HOME}/.shpotify.cfg`

ENJOY!

![terminal](https://github.com/sunnyshikhar/dotfiles/blob/master/terminal.png)