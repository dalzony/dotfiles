# dotfiles

```
ln -s dotfiles/spacemacs .spacemacs
ln -s dotfiles/zshrc .zshrc
```

## spacemacs

- emacs에서 `SPC` 대신 `M-m`

### paredit mode 에서 paredit-forward-slurp-sexp 단축키가 동작하지 않을 때

- 설정은 잘 되어 있는 것 같은데 `Ctrl+->`가 안먹을 때가 있다.
  - <img width="312" alt="2018-07-28 1 43 51" src="https://user-images.githubusercontent.com/562341/43353230-db6a334c-926d-11e8-8cf8-8a34ebd1c435.png">
- Mac OSX 를 사용하고 있다면 Mission Control의 단축키가 보통 이것으로 설정 되어있기 때문
- Preferences > Keyboard > Shortcuts > Mission Control 에서 다음 설정을 해제
<img width="404" alt="2018-07-28 1 52 48" src="https://user-images.githubusercontent.com/562341/43353231-e02a7770-926d-11e8-9a71-5654044ff4eb.png">

### font

- https://github.com/adobe-fonts/source-code-pro

```
brew tap caskroom/fonts && brew cask install font-source-code-pro
```

## zsh - theme(hyperzsh)

```
if you're using oh-my-zsh, follow these steps to install hyperzsh:

mkdir $ZSH_CUSTOM/themes You can skip this command if the directory exists already
wget -O $ZSH_CUSTOM/themes/hyperzsh.zsh-theme https://raw.githubusercontent.com/tylerreckart/hyperzsh/master/hyperzsh.zsh-theme
vim ~/.zshrc
Set ZSH_THEME="current_theme" to ZSH_THEME="hyperzsh"

```

### hyperzsh theme prompt 수정하기

- .oh-my-zsh/custom/themes/hyperzsh.zsh-theme
- 다음부분을 추가해서 `PROMPT`를 대체

```
PROMPT='$(_python_venv)%{$fg[cyan]%}%c $(git_prompt_info)%{$reset_color%}%{$fg[magenta]%}$(_git_time_since_commit)$(git_prompt_status)${_return_status}➜ '
```

- _user_host() 함수 부분을 수정할 수 있다.
- prompt 표현법은 다음 링크에서 확인 가능 
- http://zsh.sourceforge.net/Doc/Release/Prompt-Expansion.html
