# git-delete

## Delete merged branches in local

This command deletes all branches that are merged into `develop` branch.

```
$ git switch develop
$ git branch --merged | fgrep -v develop| xargs git branch -d
```

ref. [How can I delete all Git branches which have been merged? | Stackoverflow](https://stackoverflow.com/questions/6127328/how-can-i-delete-all-git-branches-which-have-been-merged)
