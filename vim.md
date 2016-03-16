## vim

 - [Close html tags](### Close html tags)
 - [List registers](### List registers)
 - [Manipulating windows](### Manipulating windows)
 - [Move the cursor before a selected character](### Move the cursor before a selected character)
 - [Paste from insert mode](### Paste from insert mode)
 - [Print the output of an external command](### Print the output of an external command)
 - [Show the path of the current file](### Show the path of the current file)

---

### Close html tags
While in insert mode, to close automatically a matching html tag just start typing `</` and then:
```
Ctrl-x Ctrl-o
```
`Ctrl-x` will put vim in completion mode and `Ctrl-o` serves as the omni completion.

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

### Show the path of the current file
In normal mode, enter the following to get the full path of the current file in the buffer:

```
:echo expand(‘%:p’)
```

If you want to show the path of the file relative to the current directory:

```
:echo @%
```
