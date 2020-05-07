# command cheat sheets table

in this file i'm going to write down every comand i learn

--------------------------------------------------------------------------------

## help commands

| command | description                                                                                                         | structure              | example                     | detail ID
|---------|---------------------------------------------------------------------------------------------------------------------|------------------------|-----------------------------|----------|
| man     | man or manual use for accessing to manual documentation of certain command                                          | man + `<command name>` | man mkdir or man cd         |          |
| --help  | using this option with any command print all options and command structure on terminal without wrapping current tab | command + `--help`     | sshfs --help or cd --help   |          |
| whatis  | use to ask for short description of any command                                                                     | whatis + `<command>`   | whatis man or what is mkdir |          |

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## directories and files modification commands

| command   | description                                                                                                                                   | structure                                             | example                                                  | detail ID                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|----------------------------------------------------------|:---------------------------------:|
| cd        | cd stands for *change directory* use for changing current path to another place in user machine                                               | cd + `path address`                                   | cd /mnt/c/Users/add/appData                              |                                   |
| cd ../    | use to get back to upper level in directory tree                                                                                              | cd ../../                                             |                                                          |                                   |
| cd ./path | means the path i'm going to go there begins from here, it can help you to write shorten path                                                  | cd ./path                                             | cd ./microsoft/help                                      |[current path](#extra_01)          |
| cd ~      | tilda in commands means home of operation system, so if you want to get back to home directory just write this symbol beside *cd* command     | cd + `~`                                              |                                                          |                                   |
| cd /      | if you put a single *slash* as an argument for cd, means you want to go to the [root](https://en.wikipedia.org/wiki/Root_directory) of system | cd / or cd /path                                      |                                                          |                                   |
| mkdir     | mkdir or *making directory* use for creating an empty directory in certain path                                                               | mkdir + directory name or mkdir + path/directory name | mkdir hello or mkdir /mnt/c/hello                        |                                   |
| mkdir .   | if you put `.` at the first of directory name or even file name, operation system hide you file or directory                                  | mkdir `.filename`                                     | mkdir /etc/.resolv.conf                                  |                                   |
| touch     | using `touch` you can create any file with any file extenstions. for example touch index.js                                                   | touch `<file name>` `<file name>`                     | touch index.js or touch /mnt/f/index.js /mnt/f/index.htm |                                   |
| rm        | rm or *remove* use to remove a directory or a file, you can also remove multiple directory or files at once                                   | rm + directory path or file name                      | rm /mnt/f/ss.txt                                         |                                   |
| rm -r     | option `-r` use to remove a directory or couple of directories(you can't remove directory without this option)                                |                                                       |                                                          |                                   |
| rm *      | `*` means all, you can remove all files or all directory without writing every directory name                                                 | rm + * or rm + *.`suffix`                             | rm *.mp4 (remove all mp4 files)                          |                                   |
| pwd       | print working directory or `pwd` uses for printing current directory path on terminal                                                         | pwd                                                   |                                                          |                                   |
| mv        | use mv or *move* to cut or move a file or directory to another place or renaming file or directory                                            | mv + path + new path or mv + file name + new name     | mv ./ss.txt /etc/ or mv ./ss.txt ./index.txt             | [move command](#extra_02)         |
| cp        | copy file or directory to another directory                                                                                                   | cp `file name` + `new directory`                      |                                                          |                                   |
| nano      | simple text editor in terminal                                                                                                                | nano + `file name`                                    |                                                          |                                   |
| nano -m   | using `-m` option enable mouse integration in nano or simply you can now use mouse to move caret                                              | nano -m `file name`                                   |                                                          |                                   |
| ls        | use to list directory containers                                                                                                              | ls `directory name` or ls `/path`                     | ls ./ or ls ../images or ls                              |                                   |
| ls -a     | using `-a` option list hidden files and directories along others                                                                              | ls -a `directory name`                                |                                                          |                                   |
| ls -l     | use to list with extra description like permissions and date modification and so on                                                           | ls -l or ls -l `directory name`                       |                                                          |                                   |
| cat       | using cat, you can print any file content inside terminal                                                                                     | cat `file name`                                       |                                                          |                                   |
| sed       | using sed you can change part of text with given parameters(very interesting command)                                                         |                                                       |                                                          | [everything about sed](#extra_02) |




