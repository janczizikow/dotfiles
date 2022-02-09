# dotfiles

## Installation

```sh
xcode-select --install

# Brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew bundle
brew services start postgresql
brew services start redis

# zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# generate a new ssh key:
# https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

# clone dotfiles and install dotfiles in preferred directory
git clone git@github.com:janczizikow/dotfiles.git
zsh install.sh

# setup git
git config --global user.email <EMAIL_HERE>
git config --global user.name <NAME_HERE>

# GPG commit signing
# see https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-gpg-key
# or change `gpgsign = true` to `gpgsign = false` in ~/.gitconfig

# macOS stuff
# Save screenshots to ~/Pictures/Screenshots
defaults write com.apple.screencapture location "${HOME}/Pictures/Screenshots"
```

## Ruby

Pick a ruby version and install it with `rbenv`

```sh
rbenv install x.x.x
rbenv global x.x.x
```

Install some gems

```sh
sudo gem install cocoapods
gem install rake bundler rspec rubocop rubocop-performance pry pry-byebug hub colored http
```