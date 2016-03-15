# vim

## Show the path of the current file
In normal, enter the following to get the full path of the current file in the buffer:

```
:echo expand(‘%:p’)
```

If you want to show the path of the file relative to the current directory:

```
:echo @%
```
