# NTUOSS-Vim-Emacs
This is a repository to try Vim and Emacs for my next TGIFHacks event.
From the start of this semester, I will try my best to devote half an hour (sounds like a good leisure time) to learn about Vim and Emacs, and hopefully record my learnings and better prepared for 2019 TGIFHacks fully.
As time went by this README.md may be editted on emacs fully. I do hope that I will truly appreciate and make full use of Vim and Emacs. 

# Vim
> As I am already using Vim, I will fullfill this section later when I am available to learn fully (not fully but in a  more comprehensive sense) about Vim.
### Exit from Vim
`Do you want to terminate running processes in this window?`
Every time has to force quite is a nightmare.
If there is only one (two) command you need to remenber for Vim it will be:
`:wq` type `:` followed by `w` and `q`
`w` means save
`q` means quit
> In some case you may not be able to write the file since you do not pocess certern priviledge, you will need to type `:q!`, which stands for discard all changes and force quit.

# Emacs
## Installing Emacs
> Mac has emacs pre-installed but the version is 22, and the version at the time is 26. Mac user can choose to update or not.
* `Windows` It seems that windows user has to install a seperate Emacs app. I will explore more on whether emacs works on bash version of windows when I get to that point. [reference](http://gnu.c3sl.ufpr.br/ftp/emacs/)
* `Mac` I update my emacs version from a third party repo. And it works fine. User need to have homebrew installed. [reference](https://github.com/railwaycat/homebrew-emacsmacport)
* `Linux` Installation is the same as windows install. I will check if the same method also apply to Linux. (I do believe some Linux distro should have Emacs pre-installed already.) [reference](http://gnu.c3sl.ufpr.br/ftp/emacs/)

## Essential Operation Instruction:

### Key alias explanation
`C-` for Holding Control.
`M-` for Holding Meta Key (META EDIT ALT key) for mac users it is option key and has to be configured according to issue #1.
`s-` referencing to super key which is command key for mac (only?).

### Exit from emacs
`Do you want to terminate running processes in this window?`
Every time has to force quite is a nightmare.
If there is only one command you need to remenber it will be:
`C-x C-c`: Type `Control + x` first and then `Control + c` to exit from emacs

## Part one: Reference to Emacs Editor tutorial

### Issue **Mac** #1: For mac users, Meta key should be set to use emacs command.
* Open Terminal and pull down the primary Terminal menu to choose “Preferences”
* Under the “Profiles” section, find your default Terminal and click the “Keyboard” subsetting tab
* Check the little box for “Use option as meta key” at the bottom of the window
* [reference](http://osxdaily.com/2013/02/01/use-option-as-meta-key-in-mac-os-x-terminal/)

