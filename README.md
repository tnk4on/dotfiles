# Personalizing with dotfile repositories

## for DevContainers
- [Developing inside a Container using Visual Studio Code Remote Development](https://code.visualstudio.com/docs/remote/containers#_personalizing-with-dotfile-repositories)
- [VSCode Remote Containersに自分のdotfilesを持ち込む - Kesinの知見置き場](https://kesin.hatenablog.com/entry/2020/07/10/083000)

## for zsh

```
mkdir ~/.zsh
cd ~/.zsh
curl -LO https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh
vi ~/.zshrc
```

~/.zshrc
```
. ~/.zsh/git-prompt.sh
GIT_PS1_SHOWDIRTYSTATE=true
GIT_PS1_SHOWUNTRACKEDFILES=true
GIT_PS1_SHOWSTASHSTATE=true
GIT_PS1_SHOWUPSTREAM=auto
setopt PROMPT_SUBST ; PS1='[%F{green}%m%f: %F{cyan}%~%f]%F{magenta}$(__git_ps1 "(%s)")%f%% '
```
