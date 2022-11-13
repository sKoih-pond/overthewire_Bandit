# Bandit Level 8 >> Level 9

### Level Goal

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once


## Walkthrough

After login with the password from [Bandit 7](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit8.md), `ls -al` displays the text file "data.txt". We will be searching for unique line of text for the password.

![File sort](/Bandit/BanditAssets/bandit9.png)

Taking a look at the file with the `head` command reveals the file has lines of hash strings to sort through.

Our solution has 2 parts:
`sort` arranges the contents by numerical and alphabetical order. This will group duplicates together.
`uniq -u` filters duplicates from our sorted list. The `-u` flag outputs only unique lines.

A single line is returned, which is the password for [Bandit 9](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit10.md).