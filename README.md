# NTUOSS Emacs Workshop

**by [Zayn Jarvis](https://github.com/ZaynJarvis) from [NTU Open Source Society](https://www.ntuoss.com)**

![](http://spacemacs.org/img/screenshots/ss1.png)

Artwork by ...

---

### Workshop Details

**When**: Friday, 8 Feb. 2019. 6:30 PM - 8:30 PM.
**Where**: LT1, NTU North Spine Plaza
**Who**: NTU Open Source Society

**Questions**: We will be hosting a Pigeon Hole Live for collecting questions regarding the workshop.

Feedback & Error Reports: We will send out the link for collecting feedback as usual. ​For further discussion or cooperation please contact @ [zaynjarvis@gmail.com](zaynjarvis@gmail.com).

**_Disclaimer: This workshop is for educational purposes only. The workshop structure is inspired by Emacs official tutorial. No prototype or outcome of any type is intended for commercial use._**

---

### Agenda
* Introduction to extensible editor: EMACS
    * Use case:
    * Key differences:
* Basic command practice with EMACS
    * File system navigation
    * move cursor
    * edit files
    * search
    * open multiple windows
* Introduction of build-in packages system ELPA
* Download external packages with MELPA
    * edit configuration files
    * understand configuration files
* A taste of org mode of EMACS
    * open org mode file
    * read org mode manual and try out org mode

---

## Introduction

EMACS is an editor with plugin system that can

1. run in bash (terminal)
2. customize anything (UI and functionality)
3. get rid of mouse (kick-ass programmer loves that)
4. be an IDE
5. be a file manager
6. be a browser
7. and many more...

For more detailed information you can go for the reference [here](https://batsov.com/articles/2011/11/19/why-emacs/)

![](https://imgs.xkcd.com/comics/real_programmers.png)

## Getting Started

### Installing Emacs

- `Windows` It seems that windows user has to install a seperate Emacs app. I will explore more on whether emacs works on bash version of windows when I get to that point. [reference](http://mirror.us-midwest-1.nexcess.net/gnu/emacs/windows/emacs-26/)
- `Mac` I update my emacs version from a third party repo. And it works fine. User need to have homebrew installed. [reference](https://github.com/railwaycat/homebrew-emacsmacport)  
> Mac has emacs pre-installed but the version is 22, and the version at the time is 26. Mac user can choose to update or not.  
```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew tap railwaycat/emacsmacport
$ brew install emacs-mac
```  
> When copying commands do not copy the `$` sign. It is a command prompt sign! I add it in purpose to show you that it is a common indicator.
- `Linux` Since Linux has the same bash environment as Mac, you can install emacs with the following command. [reference](https://medium.com/@zaynjarvis/setting-up-tensorflow-server-with-docker-part-2-d48bef8976d5)  
```bash
sudo apt-get update && sudo apt install emacs
```  
```bash
$ sudo add-apt-repository ppa:kelleyk/emacs && sudo apt-get update && sudo apt install emacs26
```
- `Online` In case you cannot set up Emacs properly in your machine, you may visit [an online emacs editor](https://www.rollapp.com/) for this workshop. And try to set up your own machine later.

### installing packages

In this section we will install markdown mode as a example to install new packages and make use of them.

1. add following content into `~/.emacs` file
   ```lisp
   (require 'package)
   (add-to-list 'package-archives
                '("melpa" . "http://melpa.org/packages/") t)
   (package-initialize)
   ```
2. reopen emacs
3. run command in emacs `M-x package-refresh-contents`
4. run command `M-x package-install <RETURN> markdown-mode <RETURN>`
5. `C-x C-f fundamental.md`
6. Now you should be viewing markdown file in markdown mode
7. Go for the document [here](https://github.com/jrblevin/markdown-mode)

# Issues

### Issue **Mac** #1: For mac users, Meta key should be set to use emacs command.

- Open Terminal and pull down the primary Terminal menu to choose “Preferences”
- Under the “Profiles” section, find your default Terminal and click the “Keyboard” subsetting tab
- Check the little box for “Use option as meta key” at the bottom of the window
- [reference]（https://github.com/jrblevin/markdown-mode)
