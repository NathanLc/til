## Unix/Bash

 - [Check that a package is installed (Ubuntu)](#check-that-a-package-is-installed-(ubuntu))
 - [Find folders not matching patterns and delete them](#find-folders-not-matching-patterns-and-delete-them)

---

### Check that a package is installed (Ubuntu)
dpkg -s <package_name>


### Find folders not matching patterns and delete them

```
find . -maxdepth 1 -type d ! -iname "<pattern1>" ! -iname "<pattern2>" -exec rm -rf "{}" \;
```

Pass the -maxdepth 1 option to the find command to restrict the search and delete to the current folder
