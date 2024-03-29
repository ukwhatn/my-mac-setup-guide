# ukwhatn's mac setup guide

## 1. Homebrew
```sh
# Install
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Add path to zsh
# ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"

# Reload shell
```

## 2. Fish shell
```sh
# Install fish
brew install fish
sudo echo "/opt/homebrew/bin/fish" | sudo tee -a /etc/shells
chsh -s /opt/homebrew/bin/fish

# Install fisher
curl https://git.io/fisher --create-dirs -sLo ~/.config/fish/functions/fisher.fish

# Install plugins
brew install z
fisher install jethrokuan/z

# Change shell to fish

# Install tide
fisher install IlanCosman/tide@v6

# Add path to fish
# nano ~/.config/fish/config.fish
eval "$(/opt/homebrew/bin/brew shellenv)"

# Reload shell
```


## 3. asdf
```sh
# Install
brew install asdf

# Add path to fish
# ~/.config/fish/config.fish
source /opt/homebrew/opt/asdf/libexec/asdf.fish
fish_add_path /Users/ukwhatn/.asdf/shims

# Load path
source ~/.zprofile
```

## 4. Install Applications
```sh
# Download Brewfile
curl https://raw.githubusercontent.com/ukwhatn/my-mac-setup-guide/main/Brewfile > ~/.Brewfile

# Install
sudo softwareupdate --install-rosetta
brew bundle --global

# Add Pathes to fish
# ~/.config/fish/config.fish
fish_add_path "/Users/ukwhatn/Library/Application Support/JetBrains/Toolbox/scripts"
fish_add_path /opt/homebrew/opt/libpq/bin
```
