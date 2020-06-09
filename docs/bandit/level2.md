# Bandit - Level 2

?> **Level Goal:** The password for the next level is stored in a file called spaces in this filename located in the home directory

Like the first two levels, the purpose of this level is to familiarize ourselves with the `ls` and `cat` command.<br>
But before we can find it, we have to connect in `ssh`.
```
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
We enter the password, which is: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`
We are now connected!

If we execute the `ls` command, we get the result.
```
bandit2@bandit:~$ ls
spaces in this filename
```

This file can be confusing because it looks like several files.

To retrieve its contents, a simple `cat` command sufit.

```
bandit2@bandit:~$ cat spaces\ in\ this\ filename 
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

The password for the levels is as follows is: `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`<br>
So you can log out with the `logout` command.