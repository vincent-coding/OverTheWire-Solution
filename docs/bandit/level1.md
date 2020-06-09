# Bandit - Level 1

?> **Level Goal:** The password for the next level is stored in a file called - located in the home directory

This level is the same difficulty as the first one.

We launch a terminal and log on.

```
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

We enter the password, which is: `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`<br>
We are now connected!

When you run the `ls` command, you get a file that appears.

```
bandit1@bandit:~$ ls
-
```

We just have to execute the `cat` command on the file to get its contents.

```
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```
The password is: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`. <br>
We have the key for level 2, we can log out with the command `logout`.