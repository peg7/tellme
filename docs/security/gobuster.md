# gobuster

https://github.com/OJ/gobuster
Directory/File, DNS and VHost busting tool written in Go

## dir MODE

```
$ gobuster -u http://fakebank.com -w wordlist.txt dir
```

- `-u` is used to state the website we're scanning.
- `-w` takes a list of words to iterate through to find hidden pages.
- `dir` means that it runs at the classic directory brute-forcing mode.

I run the command in TryHackMe/Intro to Offensive Security course.
