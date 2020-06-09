# Bandit - Level 3

?> **Level Goal:** The password for the next level is stored in a hidden file in the inhere directory.

This level will teach us how to use the `cd` command.<br>
But first you have to log in!
```
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

The password found in the previous levels is: `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`<br>
We are now connected to the server.

Once logged in, using the `ls` command, you can see that a folder with the name `inhere` exists.<br>
We're going to use the `cd` command to get into it.
```
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ 
```

Once in the folder, we'll execute the `ls` command.<br>
Unfortunately he can't find any files

Maybe a file is hidden?<br>
To find out for sure, let's run the `ls` command with the `-a` parameter.
```
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
```

Indeed, a document named .hidden was in the folder let's use the `cat` command to see the contents.
```
bandit3@bandit:~/inhere$ cat .hidden 
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```
So the password which is `pIwrPrtPN36QITSp3EQaw936yaFoFgAB` was in that hidden file.<br>
So we can disconnect, with the `logout` command.