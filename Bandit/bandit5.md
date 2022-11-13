# Bandit Level 4 >> Level 5

### Level Goal

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.


## Walkthrough

After using the password from [Bandit 3](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit3.md), `ls -alR` displays a directory with 10 files which we need to check for human-readable content.

![Scoping](/Bandit/BanditAssets/bandit5a.png)

We use the `file` command to determine the type for a given file. Here, we scope all the files in the directory using the `*` wildcard character.

![Finding](/Bandit/BanditAssets/bandit5b.png)

ASCII text indicates a human-readable file type. After using the `cat` command on "-file07", we have the password for [Bandit 5](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit6.md).