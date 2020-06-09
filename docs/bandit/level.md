# Bandit - Level 0

?> **Level Goal:** The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

This first level is very simple, its purpose is to introduce you to the `ssh` command.

To resolve this level, you need to launch a terminal and then execute this command.
<br>This command `ssh` is very important, it will connect you to the next level.

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

You will be asked for a password, enter the following password: `bandit0`.<br>
If you have entered the correct password, and the correct order you will be logged in.<br>
Now all they have to do is retrieve the passwords for the next level.

If you run the `ls` command at the root you will find a file named `readme`.<br>
Open it by executing the following command:

```
cat readme
```

The command should return the password for the next level.

```
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

So the password for level 1 is: `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`
To disconnect from the server, execute the `logout` command.

You can now proceed to Level 1!