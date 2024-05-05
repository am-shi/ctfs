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
It mentions something about a plan so look at the 'plan' file that we got:
![alt text](image-5.png)

Looks like it also needs to be decoded:

![alt text](image-7.png) 

```
IUSEDTHEPROGRAMANDHIDITWITH-DUEDILIGENCE.CHECKOUTTHEPHOTOS


```
Ok, so lets check out our program.deb file since it's mentioning it:

They're mentioning steghide-let's use it to extract the flag and since we need a password it let's try using "DUEDILIGENCE" as our passphrase:

![alt text](image-8.png)

![alt text](image-9.png)

![alt text](image-10.png) 





## Flag


##end
   