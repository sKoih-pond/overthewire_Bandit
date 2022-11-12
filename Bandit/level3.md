# Bandit Level 2 >> Level 3

### Level Goal

The password for the next level is stored in a file called **spaces in this filename** located in the home directory


## Walkthrough

After logging in from the [Bandit 2](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/level2.md) lab, a `ls -al` command on the home directory lists the file "spaces in this filename" mentioned from the Level Goal.

![Command breakdown](/Bandit/BanditAssets/level3.png)

Spaces are used to split arguments within a command. When handling files with whitespace, it is recommended to use `tab` for auto-completion.

Here there are 2 ways to navigate the whitespace:<br>
1. Using the `/` backslash character preserves the literal value of the following space
2. Enclosing the filename in `" "` doublequotes will insert the phrase as a single string

In both cases, `tab` auto-complete saves much trouble to obtain the key for the next lab, [Bandit 4](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/level4.md).


