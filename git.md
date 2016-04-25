## git

 - [Remove folder from remote](#user-content-remove-folder-from-remote)

---


### Remove folder from remote
If you do not want to track a folder but it has already been commited and you want to remove it from the remote repository, do the following:

```
git rm -r --cached <directory>
git commit -m <message> <directory>
git push origin master
```
