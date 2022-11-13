# Bandit Level 6 >> Level 7

### Level Goal

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size


## Walkthrough

After login with the password from [Bandit 5](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit5.md), `ls -al` displays a home directory with minimal content. We will have to expand our search to filter the system files.

![Command breakdown](/Bandit/BanditAssets/bandit7.png)

Searching through the `/` root directory, we input our 3 parameters from the Level Goal. `2>/dev/null` discards error outputs, which leaves 1 file to match with our criteria. This contains the password for [Bandit 7](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit8.md).