# JS_30_challenge

Based upon wesbo's [30-day JS challenge](https://javascript30.com/). His [repo](https://github.com/wesbos/JavaScript30)

I downloaded his entire repo, removed all the solutions, then redid the directories to no longer have spaces.

Removing solutions:

```shell
rm */'index-FINISHED.html'
```

[Renaming stuff:](https://unix.stackexchange.com/questions/223182/how-to-replace-spaces-in-all-file-names-with-underscore-in-linux-using-shell-scr)

```shell
find -name "* *" -print0 | sort -rz | \
  while read -d $'\0' f; do mv -v "$f" "$(dirname "$f")/$(basename "${f// /_}")"; done
```
