## Description
Figure out how they moved the

File: [Image](https://mercury.picoctf.net/static/ed308d382ae6bcc37a5ebc701a1cc4f4/tftp.pcapng)

## Hints

1. None...


## Solution
Download the file and open it up with Wireshark.Filter the packet captures to see the files that were sent & received :
```bash
$ tftp.type
```
![alt text](image-1.png)
These are the files.Export them: File -> Export Object -> TFTP
![alt text](image.png)

Look at the instructions text file first:
![alt text](image-3.png)

Decode it on cyberchef(ROT13 Encoding):
![alt text](image-4.png)
```
TFTP DOESNT ENCRYPTOURTRAFFICSOWEMUSTDISGUISEOURFLAGTRANSFER.FIGUREOUTAWAYTOHIDETHEFLAGANDIWILLCHECKBACKFORTHEPLAN
```

## Flag


##end
   