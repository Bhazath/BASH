# ~/.bashrc: executed by bash(1) for non-login shells.

# If not running interactively, don't do anything
case $- in
    *i*) ;;
      *) return;;
esac

# Set a Zsh-like prompt for Bash
# Typically, Zsh in Kali Linux uses a format like user@hostname:~/current_directory$
PS1='\[\e[1;32m\]\u@\h\[\e[0m\]:\[\e[1;34m\]\w\[\e[0m\]\$ '
 
# Enable colors for ls and other commands
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    alias dir='dir --color=auto'
    alias vdir='vdir --color=auto'
    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi
 
# User specific aliases and functions
alias ll='ls -alF' 
alias la='ls -A'
alias l='ls -CF'
alias ..='cd ..'
alias ...='cd ../..'    
alias grep='grep --color=auto'
alias df='df -h'
alias du='du -h'
alias free='free -m'
alias c='clear'
alias h='history'  
alias j='jobs -l'
alias vi='vim'   
alias update='sudo apt update && sudo apt upgrade -y'   

 # Enable bash completion
if [ -f /etc/bash_completion ]; then
    . /etc/bash_completion
fi
 
# Enable persistent history
shopt -s histappend
HISTSIZE=1000
HISTFILESIZE=2000
PROMPT_COMMAND="history -a; history -n; $PROMPT_COMMAND"

# Load additional configurations from ~/.bashrc_custom if present
if [ -f ~/.bashrc_custom ]; then
    . ~/.bashrc_custom
fi

# Export PATH
export PATH=$HOME/bin:$PATH
