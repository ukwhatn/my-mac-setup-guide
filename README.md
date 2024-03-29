# ukwhatn's mac setup guide

## 1. Homebrew
```sh
# Install
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Add path to zsh
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile

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
echo "# brew
eval \"$(/opt/homebrew/bin/brew shellenv)\"" >> ~/.config/fish/config.fish

# Reload shell
```


## 3. asdf
```sh
# Install
brew install asdf

# Add path to fish
echo "# asdf
source /opt/homebrew/opt/asdf/libexec/asdf.fish" >> ~/.config/fish/config.fish

# Load path
source ~/.zprofile
```

## 4. Install Applications
```sh
# Download Brewfile
curl https://raw.githubusercontent.com/ukwhatn/my-mac-setup-guide/main/Brewfile > ~/.Brewfile

# Install
brew bundle --global

# Add Pathes to fish
echo "# jetbrains
fish_add_path \"/Users/ukwhatn/Library/Application Support/JetBrains/Toolbox/scripts\"
# libpq
fish_add_path /opt/homebrew/opt/libpq/bin" >> ~/.config/fish/config.fish
```
