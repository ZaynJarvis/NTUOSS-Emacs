# NTUOSS Emacs Workshop

**by [Zayn Jarvis](https://github.com/ZaynJarvis) from [NTU Open Source Society](https://www.ntuoss.com)**

![](http://spacemacs.org/img/screenshots/ss1.png)

Artwork by ...

---


| Workshop Details |                                                                                       |
| :---:            | ---                                                                                   |
| When             | Friday, 8 Feb. 2019. 6:30 PM - 8:30 PM                                                |
| Where            | LT1, NTU North Spine Plaza                                                            |
| Who              | NTU Open Source Society                                                               |
| Questions        | We will be hosting a Pigeon Hole Live for collecting questions regarding the workshop |


Feedback & Error Reports: We will send out the link for collecting feedback as usual. ​For further discussion or cooperation please contact @ [zaynjarvis@gmail.com](zaynjarvis@gmail.com).

**_Disclaimer: This workshop is for educational purposes only. The workshop structure is inspired by Emacs official tutorial. No prototype or outcome of any type is intended for commercial use._**


---

### Agenda
* Introduction to extensible editor: EMACS
    * Use case
    * Key differences
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


## INSTALLATION

### Clone the repository (You will need git and a github account for this)

```bash
$ git clone https://github.com/ZaynJarvis/NTUOSS-Emacs.git
$ cd NTUOSS-Emacs/
```

### Install Emacs

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

## BASIC TUTORIAL

### Alias explanation

| Command | Description                                                                         |
| :---:   | ---                                                                                 |
| `C-`    | for Holding Control                                                                 |
| `M-`    | for Holding Meta Key (META EDIT ALT key) For mac, you may need to refer to Issue #1 |
| `s-`    | referencing to super key which is command key for mac (only?)                       |
| `S-`    | referencing to shift key                                                            |

### Open & Close Emacs

| Command   | Description                                                        |
| :---:     | ---                                                                |
| `$ emacs` | open emacs in terminal                                             |
| `C-z`     | temporary exit from emacs                                          |
| `$ fg`    | reload emacs process                                               |
| `C-x C-c` | Type `Control + x` first and then `Control + c` to exit from emacs |

> From here, we will use Emacs built-in tutoial as a guide, since it's truely awesome!

Open the editor with
`$ emacs`
Then type `C-h t` to go to the tutorial page.

### Cursor Movement

| Command | Description                                                   |
| :---:   | ---                                                           |
| `C-v`   | next page                                                     |
| `M-v`   | previous page                                                 |
| `C-l`   | command can be used three times to position the selected line |
| `C-f`   | forward                                                       |
| `C-b`   | back                                                          |
| `C-p`   | previous line                                                 |
| `C-n`   | next line                                                     |
| `C-a`   | start of the line                                             |
| `C-e`   | end of the line                                               |
| `M-f`   | forward one word                                              |
| `M-b`   | backward one word                                             |
| `M-a`   | start of the sentence                                         |
| `M-e`   | end of the sentence                                           |

### Windows (frames)

| Command        | Description                   |
| :---:          | ---                           |
| `C-x <NUMBER>` | create multiple windows       |
| `C-x o`        | change cursor to other window |
| `C-M-v`        | scroll page for other window  |

### File Editing

| Command   | Description                      |
| :---:     | ---                              |
| `C-x C-f` | Find a file                      |
| `C-x C-s` | save a file                      |
| Buffers   |                                  |
| `C-x C-b` | list buffers                     |
| `C-x b`   | switch buffer files              |
| `C-x s`   | prompt to save all buffers       |
| Editing   |                                  |
| `<DEL>`   | delete previous char             |
| `C-d`     | delete next char                 |
| `C-k`     | kill to the end of the line      |
| `M-<DEL>` | kill previous word               |
| `M-d`     | kill next word                   |
| `M-k`     | kill to the end of the sentence  |
| `C-y`     | yank last killed content         |
| `M-y`     | swich to previous killed content |
| `C-@`     | set highlight mark               |
| `C-w`     | cut                              |
| `M-w`     | copy                             |

### Search

1. `C-s`/`C-r`: start searching
2. `put searched text`: increamental search
3. `C-s`: next occuring string
4. `<DEL>`: previous occuring string / delete string by 1 character
5. `M-%`: replace string with new string
6. `<RETURN>`: end search

## ADVANCED GUIDES

### Set Emacs as default

Paste the following line into your `~/.bashrc`

```bash
export EDITOR="emacs"
```

If you only care about function but tidyness of configuration files.

```bash
echo "export EDITOR=\"emacs\"" >> ~/.bashrc && source ./bashrc
```

By doing this, for example, you can edit your git merge message with emacs by default.

### Numeric value

- `C-u <Number>` + command
- `M-<Number>` + command

| Command                        | Description                                         |
| :---:                          | ---                                                 |
| move cursor                    |                                                     |
| `C-u 8 C-p`                    | move to 8th previous line. <Recommended>            |
| `M-9 C-n`                      | move to 9th next line.                              |
| move page                      |                                                     |
| `C-u 8 C-v`                    | move page up by 8 lines.                            |
| `C-u 8 M-v`                    | move page down by 8 lines.                          |
| move with upper margin         |                                                     |
| `C-u 8 C-l`                    | move the current line to the 8th line of the screen |
| Repeat same command by x times |                                                     |
| `C-u 8 *`                      | type `********`                                     |
| `C-u 8 <DEL>`                  | delete 8 chars                                      |

### Installing packages

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

### Change mode

| Command           | Description                            |
| :---:             | ---                                    |
| `M-x <MODE_NAME>` | (For major modes) e.g. `M-x text-mode` |
| `C-h m`           | open help menu for modes               |

## Issues

### Issue **Mac** #1: For mac users, Meta key should be set to use emacs command.

- Open Terminal and pull down the primary Terminal menu to choose “Preferences”
- Under the “Profiles” section, find your default Terminal and click the “Keyboard” subsetting tab
- Check the little box for “Use option as meta key” at the bottom of the window
- [reference]（https://github.com/jrblevin/markdown-mode)

## End Notes

Here are some personal configurations you may be curious of.

* My command prompt:
```bash
PS1='\[\033[0;36m\]\[\033[0m\033[0;36m\]\w\[\033[0;0m\]\[\033[0;33m\]\[\033[0m\033[0;33m\]$(git branch 2>/dev/null | grep '^*' | colrm 1 1 )\[\033[0;0m\] \012🦄 '
```
* My `~/.emacs.d/init.el` in init.el at root folder.

**_That's it! Thank you for coming here! Leave a star if you like! Cheers! 🎉🎉🎉_**
