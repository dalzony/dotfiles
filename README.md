# dotfiles

```
ln -s dotfiles/spacemacs .spacemacs
ln -s dotfiles/zshrc .zshrc


```

## spacemacs

- emacs에서 `SPC` 대신 `M-m`

## zsh - theme(hyperzsh)

```
if you're using oh-my-zsh, follow these steps to install hyperzsh:

mkdir $ZSH_CUSTOM/themes You can skip this command if the directory exists already
wget -O $ZSH_CUSTOM/themes/hyperzsh.zsh-theme https://raw.githubusercontent.com/tylerreckart/hyperzsh/master/hyperzsh.zsh-theme
vim ~/.zshrc
Set ZSH_THEME="current_theme" to ZSH_THEME="hyperzsh"

```

## font

- https://github.com/adobe-fonts/source-code-pro

```
brew tap caskroom/fonts && brew cask install font-source-code-pro
```

### hyperzsh theme prompt 수정하기

- .oh-my-zsh/custom/themes/hyperzsh.zsh-theme
- 다음부분을 추가해서 `PROMPT`를 대체

```
PROMPT='$(_user_host)$(_python_venv)%{$fg[cyan]%}%c $(git_prompt_info)%{$reset_color%}$(git_prompt_short_sha)%{$fg[magenta]%}$(_git_time_since_commit)$(git_prompt_status)${_return_status}➜ '
```
- _user_host() 함수 부분을 수정할 수 있다.
- prompt 표현법은 다음 링크에서 확인 가능 
- http://zsh.sourceforge.net/Doc/Release/Prompt-Expansion.html
