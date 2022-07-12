# Git hooks

参考:
- [8.3 Git のカスタマイズ - Git フック](https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%9E%E3%82%A4%E3%82%BA-Git-%E3%83%95%E3%83%83%E3%82%AF)
- [githooks](https://git-scm.com/docs/githooks)

## Change the hooks directory

https://git-scm.com/docs/git-config#Documentation/git-config.txt-corehooksPath

### Change the local hooks directory

```
$ git config --local core.hooksPath .githooks
```
