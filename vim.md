## vim

 - [Append text to a register](#user-content-append-text-to-a-register)
 - [Close html tags](#user-content-close-html-tags)
 - [Delete blank lines](#user-content-delete-blank-lines)
 - [Delete lines not containing a pattern](#user-content-delete-lines-not-containing-a-pattern)
 - [Hide search hilightning](#user-content-hide-search-highlightning)
 - [Highlight blank characters in the beginning of a line](#user-content-highlight-blank-characters-in-the-beginning-of-a-line)
 - [List registers](#user-content-list-registers)
 - [Manipulating windows](#user-content-manipulating-windows)
 - [Move the cursor before a selected character](#user-content-move-the-cursor-before-a-selected-character)
 - [Paste from insert mode](#user-content-paste-from-insert-mode)
 - [Print the output of an external command](#user-content-print-the-output-of-an-external-command)
 - [Reselect last visual selections](#user-content-reselect-last-visual-selection)
 - [Show the path of the current file](#user-content-show-the-path-of-the-current-file)
 - [Yank matches of a pattern to a register](#user-content-yank-matches-of-a-pattern-to-a-register)

---

### Append text to a register
You can append text to the register `a` for instance by doing so:

```
"Ay
```

Using the capital letter instead of the lower case letter will append text

### Close html tags
While in insert mode, to close automatically a matching html tag just start typing `</` and then:
```
Ctrl-x Ctrl-o
```
`Ctrl-x` will put vim in completion mode and `Ctrl-o` serves as the omni completion.


### Delete blank lines
Delete blank lines with the `g` command:

```
:g/^$/d
```


### Delete lines not containing a pattern
To delete lines not containing a pattern, use:
```
:g!/<pattern>/d
```


### Hide search highlightning
You can hide the text highlight temporarily by entering `:noh` in normal mode.
Pressing `n` or looking for another pattern (or something of that flavour) will automatically start again the highlight.
If you want to disable it completely: `set nohlsearch`.


### Highlight blank characters in the beginning of a line
Highlight blank characters at the beginning of a line. This could also be used in a regex.

```
/^\s\+
```


### List registers
It can be useful sometimes after deleting or yanking text to check what can be pasted.
You can do so in normal mode by entering:

```
:reg
```


### Manipulating windows
`Ctrl-w` puts vim into _windows command mode_, allowing the following modifiers:
- `Ctrl-w + R` - To rotate windows up/left.
- `Ctrl-w + r` - To rotate windows down/right.

You can also use the _windows command mode_ with navigation keys to change a window's position:
- `Ctrl-w + L` - Move the current window to the "far right"
- `Ctrl-w + H` - Move the current window to the "far left"
- `Ctrl-w + J` - Move the current window to the "very bottom"
- `Ctrl-w + K` - Move the current window to the "very top"

That can also enable you to switch from vertical to horizontal split
Check out `:help window-moving` for more information


### Move the cursor before a selected character
You can use `t` to move like you would use `f` but instead of going to the said character, the cursor will be put just before.
Likewise, you can use `T` and `F` to navigate backwards.
You can also repeat the last movement by pressing `;`.


### Paste from insert mode
While in insert mode, you can paste text from a register. This can be useful also when entering a command or a search.
Just type `Ctrl-r + reg` where reg is the register you want to paste from.
Use `"` to access the lastest yanked text.


### Print the output of an external command
In normal mode, you can print the output of an external command (i.e. bash) by entering the following:

```
:r !<external_cmd>
```

### Reselect last visual selections
In normal mode, by pressing `gv`, you can reselect the last previous visual selection.


### Show the path of the current file
In normal mode, enter the following to get the full path of the current file in the buffer:

```
:echo expand(‘%:p’)
```

If you want to show the path of the file relative to the current directory:

```
:echo @%
```

### Yank matches of a pattern to a register
You can yank every text matching a pattern to the register `a` by using the command `:g`:

```
:g/<pattern>/yank A
```

The trick is to use capital A to append to register a.
