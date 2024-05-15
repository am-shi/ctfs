## Description
This file was found among some files marked confidential but my pdf reader cannot read it, maybe yours can.

File: [Disk Image](https://artifacts.picoctf.net/c/80/Flag.pdf)

## Hints

1. None...


## Solution

```bash
$ file Flag.pdf
```
![alt text](image.png) 

Looks like it isn't even a PDF file, it's a shell archive.


```bash
$ sh Flag.pdf
```
The shell script seems to extract the contents of the archive, as indicated by the messages "x - extracting flag (text)"

## Flag


##end
   