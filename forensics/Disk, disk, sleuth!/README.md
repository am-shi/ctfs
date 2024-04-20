## Description
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk 

File: [Disk Image](https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz)

## Hints

1. Have you ever used `file` to determine what a file was?
2. Mastering this terminal-fu would enable you to find the flag in a single command


## Solution

```bash
$ gunzip dds1-alpine.flag.img.gz
$ file dds1-alpine.flag.img
$ srch_strings dds1-alpine.flag.img | grep picoCTF
```



## Flag
![alt text](image-1.png)


##end
   
   