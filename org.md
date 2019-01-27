## [Org mode](https://orgmode.org/orgguide.pdf) of emacs

### Example of org mode files

```bash
* Top level headline
** Second level
*** 3rd level
some text
*** 3rd level
more text
* Another top level headline
```

### Toggle view controls

| Command | Description |
| :---: | --- |
| `<TAB>` | cycle from `Folded` to `Children` to `Subtree` back to `Folded` |
| `S-<TAB>` `C-u <TAB>` | global cycling |

### Motion

| Command | Description |
| :---: | --- |
| `C-c C-n` | Next heading. |
| `C-c C-p` | Previous heading. |
| `C-c C-f` | Next heading same level. |
| `C-c C-b` | Previous heading same level. |
| `C-c C-u` | Backward to higher level heading. |
| `C-c C-j` | (org-goto) |

> Jump to a different place without changing the current outline visibility.

> Shows the document structure in a temporary buffer, where you can use the following keys to find your destination:
	* `TAB`	Cycle visibility.
	* `DOWN / UP`	Next/previous visible headline.
	* `RET`	Select this location.
	* `/`	Do a Sparse-tree search
