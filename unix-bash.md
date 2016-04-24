## Unix/Bash

 - [Check that a package is installed (Ubuntu)](#user-content-check-that-a-package-is-installed-(ubuntu))
 - [Delete word behind cursor in cli](#user-content-delete-word-behind-cursor-in-cli)
 - [Display line numbers in less](#user-content-display-line-numbers-in-less)
 - [Find folders not matching patterns and delete them](#user-content-find-folders-not-matching-patterns-and-delete-them)
 - [Go to beginning of line in bash](#user-content-go-to-beginning-of-line-in-bash)
 - [List packages](#user-content-list-packages)
 - [Open less without line wrap](#user-content-open-less-without-line-wrap)
 - [Switch input mode in bash](#user-content-switch-input-mode-in-bash)

---


### Check that a package is installed (Ubuntu)
dpkg -s <package_name>


### Delete word behind cursor in cli
While entering a command in the termianl, you can delete the word behind the cursor by pressing `Ctrl-w`.
The whole line can be deleted by entering `Ctrl-u` instead.


### Display line numbers in less
To toggle line numbers in the left column in less, enter `-N`.
Likewise, less can be opened with the `-N` option to have line numbers displayed when opening a file.


### Find folders not matching patterns and delete them

```
find . -maxdepth 1 -type d ! -iname "<pattern1>" ! -iname "<pattern2>" -exec rm -rf "{}" \;
```

Pass the -maxdepth 1 option to the find command to restrict the search and delete to the current folder


### Go to beginning of line in bash
In bash, press `Ctrl-a` to go to the beginning of the line. Likewise, `Ctrl-e` will carry you to the end of the line.


### List packages
Display the list of packages installed or removed:

```
dpkg --get-selections
```


### Open less without line wrap
To open less without line wrap, pass the `-S` option to less. You can also toggle line wrapping by entering `-S` inside less.
You can also pipe less to the output of a command:

```
find . -name "<pattern>" -type f | xargs egrep -in "<otherpattern>" | less -S
```


### Switch input mode in bash
To switch input mode in bash (emacs or vi), enter the following command:

```
set -o <emacs/vi>
```

You can set the following option to set the default editing mode, either in your .bashrc or .inputrc for every cli program:

```
set editing-mode <emacs/vi>
```
