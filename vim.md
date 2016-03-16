## vim

### Close html tags
While in insert mode, to close automatically a matching html tag just start typing `</` and then:
```
<C-x><C-o>
```
<C-x> will put vim in completion mode and <C-o> serves as the omni completion.

### Move the cursor before a selected character
You can use `t` to move like you would use `f` but instead of going to the said character, the cursor will be put just before.
Likewise, you can use `T` and `F` to navigate backwards.
You can also repeat the last movement by pressing `;`.

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
