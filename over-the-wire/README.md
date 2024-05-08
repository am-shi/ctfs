## Over the Wire

The wargames offered by the OverTheWire community can help you to learn and practice security concepts in the form of fun-filled games.

![alt text](image.png)

## 0rder of the Games

```
(1)Bandit
(2)Leviathan or Natas or Krypton
(3)Narnia
(4)Behemoth
(5)Utumno
(6)Maze
```
## (1) Bandit

## Level 0

```bash
$ ssh bandit0@bandit.labs.overthewire.org -p 2220 
$ ls
$ cat readme
```

## Level 0 - 1

![alt text](image-1.png)



## Level 1 - 2
![alt text](image-2.png) 


## Level 2 - 3

```bash
$ ls
$ ls -al
$ cat .hidden
``` 

## Level 3 - 4

![alt text](image-3.png)


## Level 4 - 5

```
Level Goal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable
```



![alt text](image-4.png)

The du command is used to estimate file and directory space usage.


```
(1)file */{.,}*:
This command uses the file utility to determine the type of each file in the inhere directory and its subdirectories.

(2)The */{.,}* :
 Pattern expands to match all files and directories (including hidden ones starting with .) in the inhere directory and its subdirectories.

(3)grep "ASCII text":
This command filters the output of the file command to only show lines containing the string "ASCII text".

(4)grep -v ', with very long lines':
This command further filters the output to exclude lines containing the string ", with very long lines".It removes files that are identified as ASCII text but have very long lines, which may not be relevant to the task at hand.

(5)du -b -a:
This command calculates the disk usage of each file in bytes (-b) and displays all files (-a) in the current directory and its subdirectories.

(6)grep 1033:
This command filters the output of the du command to only include lines containing "1033".
It's used to identify files that are exactly 1033 bytes in size.

```

## Level 5 - 6

```
Level Goal

The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

```

![alt text](image-5.png)

```bash
$ find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

Explanation of the command:
```
find /: Starts the search from the root directory.
-type f: Specifies that we're looking for files.
-user bandit7: Filters files owned by the user bandit7.
-group bandit6: Filters files owned by the group bandit6.
-size 33c: Filters files that are exactly 33 bytes in size.

2>/dev/null: Redirects error messages (such as permission denied) to /dev/null to suppress them.
```


## Level 6 - 7


