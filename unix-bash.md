## Unix/Bash

 - [Check that a package is installed (Ubuntu)](#check-that-a-package-is-installed-(ubuntu))
 - [Delete word behind cursor in cli](#delete-word-behind-cursor-in-cli)
 - [Find folders not matching patterns and delete them](#find-folders-not-matching-patterns-and-delete-them)
 - [Open less without line wrap](#open-less-without-line-wrap)

---


### Check that a package is installed (Ubuntu)
dpkg -s <package_name>


### Delete word behind cursor in cli
While entering a command in the termianl, you can delete the word behind the cursor by pressing `Ctrl-w`.
The whole line can be deleted by entering `Ctrl-u` instead.

### Find folders not matching patterns and delete them

```
find . -maxdepth 1 -type d ! -iname "<pattern1>" ! -iname "<pattern2>" -exec rm -rf "{}" \;
```

Pass the -maxdepth 1 option to the find command to restrict the search and delete to the current folder


### Open less without line wrap
To open less without line wrap, pass the `-S` option to less. You can also toggle line wrapping by entering `-S` inside less.
You can also pipe less to the output of a command:

```
find . -name "<pattern>" -type f | xargs egrep -in "<otherpattern>" | less -S
```
