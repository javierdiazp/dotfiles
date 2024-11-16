# Dotfiles

## System settings
- Display -> Arrange monitors
- Mouse -> Natural scrolling
- Keyboard -> Modifier keys
- Dock -> Auto hide and show, show suggested and recent, click wallpaper
- Control center -> Never hide and show menu bar

## Environment

### Install Homebrew

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew bundle install
```

### Install Oh-My-Zsh and plugins
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

### Install and configure iTerm2
```
(curl -Ls https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Andromeda.itermcolors > /tmp/Andromeda.itermcolors && open /tmp/Andromeda.itermcolors)
```

### Install .dotfiles

```
git clone https://github.com/javierdiazp/dotfiles.git .dotfiles

rm -rf .gitconfig
ln -s .dotfiles/.gitconfig .gitconfig

rm -rf .zshrc
ln -s .dotfiles/.zshrc .zshrc

rm -rf .zprofile
ln -s .dotfiles/.zprofile .zprofile

rm -rf .p10k.zsh
ln -s .dotfiles/.p10k.zsh .p10k.zsh
```
