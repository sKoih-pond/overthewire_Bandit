# Bandit Level 7 >> Level 8

### Level Goal

The password for the next level is stored in the file **data.txt** next to the word **millionth**


## Walkthrough

After login with the password from [Bandit 6](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit7.md), `ls -al` displays the text file "data.txt". 

![File search](/Bandit/BanditAssets/bandit8.png)

Using the `head` command on the file displays its first 10 lines, which have random text followed by hash strings.

The `grep` command searches the file for any line which matches our input argument "millionth". This search is case sensitive and outputs a single match, which contains the password for [Bandit 8](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit9.md).
