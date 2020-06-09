# Bandit - Level 4

?> **Level Goal:** The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

This level teaches us one of the uses of the `file` command.<br>
As usual we have to connect to the level.
```
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

The password found in the previous levels is: `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`<br>
We are now connected to the server.

Always execute the `ls` command
```
bandit4@bandit:~$ ls
inhere
```
We see that a file with the name `inhere`, exists, so we're going to go into it.<br>
We use the `cd` command.
```
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ 
```
We are going to re-execute the `ls` command, to retrieve the list of files and folders from this folder
```
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
```
We see that this folder has `10 files`.

We need to find the password in his files.<br>
We can check all the files one by one with the `cat` command, but we're here to go fast, so we're going to use the `file` command.
```
bandit4@bandit:~/inhere$ file ./-*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```
As can be seen, 9 of the 10 files contain characters not readable by a human being, only 1 contains `ASCII` characters.<br>
So we're going to open it with the `cat` command.
```
bandit4@bandit:~/inhere$  cat ./-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```
And so it was the file containing the password of the next level.<br>
It is therefore possible to log out using the `logout` command.