## Essential Operation Instruction:

### Key alias explanation

| Command | Description                                                                                                             |
| :---:   | ---                                                                                                                     |
| `C-`    | for Holding Control.                                                                                                    |
| `M-`    | for Holding Meta Key (META EDIT ALT key) for mac users it is option key and has to be configured according to issue #1. |
| `s-`    | referencing to super key which is command key for mac (only?).                                                          |

### Open and close emacs

| Command   | Description                                                        |
| :---:     | ---                                                                |
| `$ emacs` | open emacs in terminal                                             |
| `C-z`     | temporary exit from emacs                                          |
| `$ fg`    | reload emacs process                                               |
| `C-x C-c` | Type `Control + x` first and then `Control + c` to exit from emacs |


### Undo

In case you did something wrong to an essential text. You do not want to force quit and take the risk that everything goes wrong.
Use following command to undo your changes.
They all behave the same use the available one in your terminal

- `C-_`
- `C-/`
- `C-x u`

## Part one: Reference to Emacs Editor tutorial

### Move page

| Command | Description                                                   |
| :---:   | ---                                                           |
| `C-v`   | next page                                                     |
| `M-v`   | previous page                                                 |
| `C-l`   | command can be used three times to position the selected line |

> put the selected line at center, top, and bottom

### Move cursor

| Command | Description           |
| :---:   | ---                   |
| `C-f`   | forward               |
| `C-b`   | back                  |
| `C-p`   | previous line         |
| `C-n`   | next line             |
| `C-a`   | start of the line     |
| `C-e`   | end of the line       |
| `M-f`   | forward one word      |
| `M-b`   | backward one word     |
| `M-a`   | start of the sentence |
| `M-e`   | end of the sentence   |

### Cut and paste

| Command   | Description                                                   |
| :---:     | ---                                                           |
| `<DEL>`   | previous char (delete only)                                   |
| `C-d`     | next char (delete only)                                       |
| `C-k`     | to the end of the line (cut)                                  |
| `M-<DEL>` | previous word (cut)                                           |
| `M-d`     | next word (cut)                                               |
| `M-k`     | to the end of the sentence (cut)                              |
| `C-y`     | yank last killed content                                      |
| `M-y`     | swich to previous killed content in a **killed content loop** |

### File

| Command               | Description                |
| :---:                 | ---                        |
| `C-x C-f <FILE_NAME>` | Find a file                |
| `C-x C-s`             | save a file                |
| `C-x C-b`             | list buffers               |
| `C-x b`               | switch buffer files        |
| `C-x s`               | prompt to save all buffers |

### Search

1. `C-s`/`C-r`: start searching
2. `put searched text`: increamental search
3. `C-s`: next occuring string
4. `<DEL>`: previous occuring string / delete string by 1 character
5. `<RETURN>`: end search

### Change mode

| Command           | Description                            |
| :---:             | ---                                    |
| `M-x <MODE_NAME>` | (For major modes) e.g. `M-x text-mode` |
| `C-h m`           | open help menu for modes               |

### Windows (frames)

| Command        | Description                   |
| :---:          | ---                           |
| `C-x <NUMBER>` | create multiple windows       |
| `C-x o`        | change cursor to other window |
| `C-M-v`        | next page for other window    |

## Pro Tips

### Numeric value

- `C-u Number Key` + command
- `M- Number Key` + command

| Command                        | Description                                         |
| :---:                          | ---                                                 |
| move cursor                    |                                                     |
| (`C-u` `8` `C-p`)              | move to 8th previous line. <Recommended>            |
| (`M-9` `C-n`)                  | move to 9th next line.                              |
| move page                      |                                                     |
| (`C-u` `8` `C-v`)              | move page up by 8 lines.                            |
| (`C-u` `8` `M-v`)              | move page down by 8 lines.                          |
| move with upper margin         |                                                     |
| (`C-u` `8` `C-l`)              | move the current line to the 8th line of the screen |
| Repeat same command by x times |                                                     |
| (`C-u` `8` `*`)                | type `********`                                     |
| (`C-u` `8` `<DEL>`)            | delete 8 chars                                      |

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
