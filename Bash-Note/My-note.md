### 1) To alias 
```
alias "name"="command"

alias install="sudo apt install"
alias e="vim,nano"
```

- add to ~/.bashrc at the end
#
### 2) Checking your weather forecast
```
alias wtr='curl wttr.in'
```
#
### 3) to check the speed test 
```
speedtest='curl -s https://raw.githubusercontent.com/sivel/speedtest-cli/master/speedtest.py | python -' #
# at last choose python3 or your specific system, python installed 
```
# - `Note` : to check the private IP info
  ```
  curl ipinfo.io
  ```
### 4) bash_prompt 

To use the same bash prompt style as Jay, create the file ~/home/.bash_prompt and place the following inside:
```
BRACKET_COLOR="\[\033[38;5;35m\]"
CLOCK_COLOR="\[\033[38;5;35m\]"
JOB_COLOR="\[\033[38;5;33m\]"
PATH_COLOR="\[\033[38;5;33m\]"
LINE_BOTTOM="\342\224\200"
LINE_BOTTOM_CORNER="\342\224\224"
LINE_COLOR="\[\033[38;5;248m\]"
LINE_STRAIGHT="\342\224\200"
LINE_UPPER_CORNER="\342\224\214"
END_CHARACTER="|"

tty -s && export PS1="$LINE_COLOR$LINE_UPPER_CORNER$LINE_STRAIGHT$LINE_STRAIGHT$BRACKET_COLOR[$CLOCK_COLOR\t$BRACKET_COLOR]$LINE_COLOR$LINE_STRAIGHT$BRACKET_COLOR[$JOB_COLOR\j$BRACKET_COLOR]$LINE_COLOR$LINE_STRAIGHT$BRACKET_COLOR[\H:\]$PATH_COLOR\w$BRACKET_COLOR]\n$LINE_COLOR$LINE_BOTTOM_CORNER$LINE_STRAIGHT$LINE_BOTTOM$END_CHARACTER\[$(tput sgr0)\] "
```
Save that file, and then open up your ~/.bashrc and place the following at the end of the file:
      
  - comment all PS1 Prompt ~/.bashrc
```
source ~/.bash_prompt
```
  - to start new bash prompt
```
exec bash
```
# 
### 5) JOBS

- jobs :- see the jobs running in background
- ctrl-z :- minimize
- fg :- forground # fg {job number}
- bg :-  Move jobs to the background.
#

### 6) to open any file in desktop linux for terminal
```
xdg-open <file>,<txt>
```
#

# *7) View Linux command cheat sheets*

**Viewing man pages might be useful, but cheat sheets are simpler and more to the point. You can view a cheat sheet from cheat.sh by running a command like the following:**
```
curl https://cheat.sh/<ls>
```
**Replace the command name at the end with the command you want to see information on.**
