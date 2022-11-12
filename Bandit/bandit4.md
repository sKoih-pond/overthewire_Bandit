# Bandit Level 3 >> Level 4

### Level Goal

The password for the next level is stored in a hidden file in the inhere directory.


## Walkthrough

Following the trend from [Bandit 3](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit3.md), an `ls -al` displays the files and directories we have to work with.

![Command breakdown](/Bandit/BanditAssets/bandit4.png)

`ls -alR` saves us an extra step by recursively listing everything within the home directory.

From here, we find the hidden file indicated by the `.` period, which contains the password for [Bandit 5](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit5.md).
