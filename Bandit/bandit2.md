# Bandit Level 1 >> Level 2

### Level Goal

The password for the next level is stored in a file called - located in the home directory


## Walkthrough

After logging in with the password from the [Bandit 0](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit0.md) lab, a `ls -al` command on the home directory lists the "-" file mentioned in the Level Goal.

![Command breakdown](/Bandit/BanditAssets/bandit2.png)

`cat -` will not show the password because the `cat` command interprets the `-` as a special character to wait for a `stdin` (standard input) to direct to `stdout` (standard output). In this case, it will repeat whatever we type to the command interface.

`Ctrl + C` will exit and free standard input again.

`cat ./-` specifies the cat command to open the "-" file from the current directory, which reveals the password for the next lab, [Bandit 2](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit2.md).