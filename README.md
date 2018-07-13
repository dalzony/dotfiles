# dotfiles

```
ln -s dotfiles/spacemacs .spacemacs
ln -s dotfiles/zshrc .zshrc


```


## zsh - theme(hyperzsh)

```
if you're using oh-my-zsh, follow these steps to install hyperzsh:

mkdir $ZSH_CUSTOM/themes You can skip this command if the directory exists already
wget -O $ZSH_CUSTOM/themes/hyperzsh.zsh-theme https://raw.githubusercontent.com/tylerreckart/hyperzsh/master/hyperzsh.zsh-theme
vim ~/.zshrc
Set ZSH_THEME="current_theme" to ZSH_THEME="hyperzsh"
```
