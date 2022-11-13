# Bandit Level 5 >> Level 6

### Level Goal

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable


## Walkthrough

After using the password from [Bandit 4](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit4.md), `ls -al` displays the "inhere" directory, which contains 20 subdirectories to search for the password file. By now, we are familiar with the `ls` command and its optional parameters.

![Screenshot](/Bandit/BanditAssets/bandit6.png)

> `find inhere/ -type f -size 1033c ! -executable -exec file {} + | grep -w "text"`

This command is more complex than the ones from previous labs. I researched the answer from [StackExchange](https://unix.stackexchange.com/questions/313442/find-human-readable-files) and [Baeldung](https://www.baeldung.com/linux/find-exec-command).

`type f` indicates we are searching for a file.

`-size 1033c` specifies for only 1033 bytes, where c denotes singular bytes

`! -executable` filters out executable permissions, this is actualy not necessary for the exercise.

Now the fun part...

`-exec file {} ` invokes a file command to the results we have filtered for, where `{}` is a placeholder for the filepath argument.

`+ | grep -w "text"` The `+` is a delimiter which joins our results into a single output, which is piped to `grep` which only lists results matching for "text" as we are searching for ASCII text.


After running the command, we have a single match for our search parameters and we obtain the password for [Bandit 6](https://github.com/sKoih-pond/overthewire_wargames/blob/main/Bandit/bandit6.md) from the file.