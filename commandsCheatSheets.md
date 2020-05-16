# command cheat sheets table

in this file i'm going to write down every comand i learn


## help commands

| command | description                                                                                                         | structure              | example                     | detail ID
|---------|---------------------------------------------------------------------------------------------------------------------|------------------------|-----------------------------|----------|
| man     | man or manual use for accessing to manual documentation of certain command                                          | man + `<command name>` | man mkdir or man cd         |          |
| --help  | using this option with any command print all options and command structure on terminal without wrapping current tab | command + `--help`     | sshfs --help or cd --help   |          |
| whatis  | use to ask for short description of any command                                                                     | whatis + `<command>`   | whatis man or what is mkdir |          |



## directories and files modification commands

| command   | description                                                                                                                                   | structure                                                                                       | example                                                  | detail ID                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------|:---------------------------------:|
| cd        | cd stands for *change directory* use for changing current path to another place in user machine                                               | cd + `path address`                                                                             | cd /mnt/c/Users/add/appData                              |                                   |
| cd ../    | use to get back to upper level in directory tree                                                                                              | cd ../../                                                                                       |                                                          |                                   |
| cd ./path | means the path i'm going to go there begins from here, it can help you to write shorten path                                                  | cd ./path                                                                                       | cd ./microsoft/help                                      |[current path](#extra_01)          |
| cd ~      | tilda in commands means home of operation system, so if you want to get back to home directory just write this symbol beside *cd* command     | cd + `~`                                                                                        |                                                          |                                   |
| cd /      | if you put a single *slash* as an argument for cd, means you want to go to the [root](https://en.wikipedia.org/wiki/Root_directory) of system | cd / or cd /path                                                                                |                                                          |                                   |
| mkdir     | mkdir or *making directory* use for creating an empty directory in certain path                                                               | mkdir + directory name or mkdir + path/directory name                                           | mkdir hello or mkdir /mnt/c/hello                        |                                   |
| mkdir .   | if you put `.` at the first of directory name or even file name, operation system hide you file or directory                                  | mkdir `.filename`                                                                               | mkdir /etc/.resolv.conf                                  |                                   |
| touch     | using `touch` you can create any file with any file extenstions. for example touch index.js                                                   | touch `<file name>` `<file name>`                                                               | touch index.js or touch /mnt/f/index.js /mnt/f/index.htm |                                   |
| rm        | rm or *remove* use to remove a directory or a file, you can also remove multiple directory or files at once                                   | rm + directory path or file name                                                                | rm /mnt/f/ss.txt                                         |                                   |
| rm -r     | option `-r` use to remove a directory or couple of directories(you can't remove directory without this option)                                |                                                                                                 |                                                          |                                   |
| rm *      | `*` means all, you can remove all files or all directory without writing every directory name                                                 | rm + * or rm + *.`suffix`                                                                       | rm *.mp4 (remove all mp4 files)                          |                                   |
| pwd       | print working directory or `pwd` uses for printing current directory path on terminal                                                         | pwd                                                                                             |                                                          |                                   |
| mv        | use mv or *move* to cut or move a file or directory to another place or renaming file or directory                                            | mv + path + new path or mv + file name + new name                                               | mv ./ss.txt /etc/ or mv ./ss.txt ./index.txt             | [move command](#extra_02)         |
| cp        | copy file or directory to another directory                                                                                                   | cp `file name` + `new directory`                                                                |                                                          |                                   |
| nano      | simple text editor in terminal                                                                                                                | nano + `file name`                                                                              |                                                          |                                   |
| nano -m   | using `-m` option enable mouse integration in nano or simply you can now use mouse to move caret                                              | nano -m `file name`                                                                             |                                                          |                                   |
| ls        | use to list directory containers                                                                                                              | ls `directory name` or ls `/path`                                                               | ls ./ or ls ../images or ls                              |                                   |
| ls -a     | using `-a` option list hidden files and directories along others                                                                              | ls -a `directory name`                                                                          |                                                          |                                   |
| ls -l     | use to list with extra description like permissions and date modification and so on                                                           | ls -l or ls -l `directory name`                                                                 |                                                          |                                   |
| cat       | using cat, you can print any file content inside terminal                                                                                     | cat `file name`                                                                                 |                                                          |                                   |
| sed       | using sed you can change part of text with given parameters(very interesting command)                                                         |                                                                                                 |                                                          | [everything about sed](#extra_03) |
| rename    | rename multiple files at once or multiple file extensions at once(it is much like sed command but for renaming)                               | rename "s/old_name/new_name/ * or rename "s/old_extensions/new_extension/" *.current_extensions | rename "s/jpg/png/" *.jpg or rename "s/flower/tree/ *    |                                   |




## ip and networking commands

| command          | description                                                                                                                                                      | structure                                                       | example                                             | detail ID |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------|-----------|
| ip a             | show all ip address with devices                                                                                                                                 | ip a                                                            |                                                     |           |
| ip a show        | using `show` option can filter specific devices                                                                                                                  | ip a show `device name`                                         | ip a show eth0                                      |           |
| ip a add         | add ipv4 address to any device you want                                                                                                                          | ip a add `<ip address>`/24 brd `xx.xx.xx.255` dev `device name` | ip a add 192.168.0.20/24 brd 192.168.0.255 dev eth0 |           |
| ip a del         | delete ipv4 address from any device                                                                                                                              | ip a del `<ip address>`/24 dev `<device name>`                  | ip a del 192.168.0.20/24 dev eth0                   |           |
| ip -4 a          | show ipv4 addresses only                                                                                                                                         |                                                                 |                                                     |           |
| ip route         | show route address or gateway of devices                                                                                                                         |                                                                 |                                                     |           |
| ip route list    | list all gateway in network devices                                                                                                                              |                                                                 |                                                     |           |
| ip r add         | add route to the specific device                                                                                                                                 | ip r add default via `<gateway address>` dev `device name`      | ip r add default via 192.168.0.1 dev eth0           |           |
| ip r del         | remove specific route from device                                                                                                                                | ip r del `<gateway address>` dev `device name`                  | ip r del 192.168.0.1 dev eth0                       |           |
| ping             | ping specific ip address or a domain name                                                                                                                        | ping `ip address` or `domain name`                              | ping google.com or ping 172.152.120.50              |           |
| ping -c          | count an ip address with custom number                                                                                                                           | ping -c `number` `ip address`                                   | ping -c 3 google.com ( call google.com 3 times)     |           |
| whoami           | ask terminal for giving your username                                                                                                                            |                                                                 |                                                     |           |
| hostname         | ask for computer name                                                                                                                                            |                                                                 |                                                     |           |
| hostname -I      | giving your hs name's ip address                                                                                                                                 |                                                                 |                                                     |           |
| curl             | using curl to upload or download from (http, https, smtp, ftp)                                                                                                   | curl `<url>`                                                    | curl https://download.com/winrar.exe                |           |
| curl -C - -O     | using options `-C - ` means continue from last seesion if download is interupted and `-O` captila o means use the default name when you're writing on my machine | curl -C - -O `<url>`                                            | curl -C - -O http://download.com/winrar.exe         |           |
| curl ifconfig.me | use to print your public ip address                                                                                                                              |                                                                 |                                                     |           |

## super power command (sudo)

| command                | description                                                                                                                              | structure                                     | example                                        | detail ID            |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------|
| sudo                   | sudo means *super user do* what i want                                                                                                  | sudo `<command>`                              | sudo mkdir                                     | [sudo](#extra_04)    |
| sudo su                | change user to `@root` for amitting sudo from any command                                                                                |                                               |                                                |                      |
| su                     | sometimes a machine has multiple user, to switch to another user you need this command                                                   | su `username`                                 | su illustray                                   |                      |
| apt                    | command line interface or a command to install or remove packages in linux distros                                                       |                                               |                                                |                      |
| apt install            | install packages from repository                                                                                                         | sudo apt install `<package name>`             | sudo apt install vlc                           |                      |
| apt -y                 | use `-y` option to pass yes if command needs permission, it gives yes to any asking for permissions                                      | sudo apt `<option>` -y                        | sudo apt install vlc -y                        |                      |
| apt remove             | remove packages                                                                                                                          | sudo apt remove `<package name>`              | sudo apt remove vlc -y                         |                      |
| apt --purge            | use this option whenever you want to remove a package, purging means ask to clear any configuration                                      | sudo apt remove --purge `<package name>` -y   | sudo apt remove --purge vlc -y                 | [purging](#extra_05) |
| apt list               | list installed or any existing packages in ubuntu repositories                                                                           | sudo apt list --installed                     |                                                |                      |
| apt --reinstall        | reinstall packages                                                                                                                       | sudo apt install --reinstall `<package name>` | sudo apt install --reinstall vlc sshfs fuse -y |                      |
| do-release-upgrade     | upgrade operation system to latest release                                                                                               |                                               | do-release-upgrade                             |                      |
| do -release-upgrade -V | show operation system version                                                                                                            |                                               |                                                |                      |
| do-release-upgrade -d  | upgrade to development release                                                                                                           |                                               |                                                |                      |
| which                  | using `which` you can find installed packages on your machine, it is useful when you want to check whether a package is installed or not | which `package name`                          | which ruby                                     |                      |
| dpkg                   | package manager for debian, if you want to install packages with `.deb` format you need this tool to accomplish your job                 | sudo dpkg `option` `<package name>`           |                                                |                      |
| dpkg -i                | install opr option `-i` use to install package on debian distros                                                                         | sudo dpkg -i `<package_name>`                 | sudo dpkg -i code.deb                          |                      |
| dpkg -r --purge        | remove package from the machine and clean package configuration on the machine                                                           | sudo dpkg -r --purge `<package_name>`         | sudo dpkg -r --purge code.deb                  |                      |

## services commands

| command               | description                                                                                            | structure                                                     | example                   | detail ID |
|-----------------------|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------|-----------|
| service               | this command gives you an ability to trun on or off the services on your machine such as apache or ssh | sudo service `<service name>` start | stop | status | restart | sudo service ssh start    |           |
| service \--status-all | use to print all services status on terminal                                                           |                                                               | sudo service --status-all |           |

## firewall commands

| commands       | description                                          | structure                      | example                           | detail ID |
|----------------|------------------------------------------------------|--------------------------------|-----------------------------------|-----------|
| ufw            | use to add or remove rule from firewall              | sudo ufw `<option>` `argument` | sudo ufw allow from 192.168.1.120 |           |
| ufw allow      | allow a specific rule to pass from firewall          | sudo ufw allow `port`          | sudo ufw allow 1920               |           |
| ufw allow from | use to allow an ip to access to specific application | sudo ufw allow from `ip add`   | sudo ufw allow from 192.168.1.150 |           |
| ufw deny       | deny a rule to pass from firewall                    | sudo ufw deny `port`           | sudo ufw deny 1102                |           |
| ufw enable     | enable firewall to work                              |                                | sudo ufw enable                   |           |
| ufw disable    | disable firewall to work                             |                                | sudo ufw disable                  |           |
| ufw reset      | reset firewall to default                            |                                | sudo ufw reset                    |           |
| ufw status     | status firewall to print all allowed or denyed rules |                                | sudo ufw status                   |           |

## shell and script commands

| commands | description                                                                                                               | structure                     | example               | detail ID |
|----------|---------------------------------------------------------------------------------------------------------------------------|-------------------------------|-----------------------|-----------|
| chsh     | chsh or *change shell* use for changing shell interface to another one in terminal, such as zsh oth-my-zsh bash and etc.. | chsh -s $(which `shell name`) | chsh -s $(which zsh)  |           |
| source   | source comamnd using for compiling and running script file like file                                                      | source `script file`          | source /etc/shell.zsh |           |
| bash     | same as *source* command it is used to run script                                                                         | bash `file .sh`               | bash run.sh           |           |
| .        | abbreviation for source command, you can simply put `.` instead of writing `source` command                               | . `script file`               | . ./install.sh        |           |

## some important notes

### how to disable ring bell inside terminal

sometimes some shells give you an annoying sound of *bib* for some actions such as pressing backward key or enter key which is so annoying, so if you want /

to **silent** your shell

> first open `/etc/inputrc` file

> then write down `set bell-style none` to silent your shell

### how to print command output as a text file

did you know that you can save your command result as a text file? if you want to not print your command result inside your shell interface, you can send to a specific text file

with specific format such as `.txt` or `.md`

for doing such a thing just use `>>` to navigate command result to a text file

for example

```
ping google.com -c 2 >> /mnt/d/pingResult.txt

echo 'how are you' >> /mnt/d/greeting.md
```
### run any command when you open a tab or start the terminal

usualy, i need to call a command in shell when i just start the terminal without rewriting or recalling a command

for example i want to print a messagge with `cowsay` command eveytime i open a terminal in my machine, for doing such a thing you simply need a `run in time` file

a `run in time` file is an essential file for running your bash inside terminal propebly well

luckily we don't need to create it because every shell has such a file, you just need to write down you specific command which you want to run everytime

default terminal which mostly call `bash` has specific file call `bashrc`, so if you put your command inside *bashrc* file you can expect terminal execute your command *automatically* everytime you create a new tab or open new terminal

*you can find `bashrc` file inside your home directory `~`*

*for a popular shell such as `zsh` you must open `zshrc` file inside home directory*

### what is *.sh* file

.sh file format is a script programmed file for a terminal, it means you can write your terminal programes or simply write bunch of commands inside this file format and

expect terminal run your commands or any script you have written inside your file

for example i can simply write `scp /mnt/d/text.md /etc/` inside *.sh* file and run the command without writting it everytime i need

it is useful when you want to call many commands at once without writing them over and over again

or even better you can create a program script file for your terminal to automate your jobs

> just simply create file with `*.sh` format like *run.sh* and call it with `bash` command

```
bash run.sh

bash shutdown.sh
```

#### using .sh file for automate jobs inside zshrc or bashrc file

just write your desire commands inside this file and call it with `bash` command inside `.zshrc` or `.bashrc` file to even run the script automatically

### <a name="extra_02></a> renaming files and directories using *mv* command
 you can also use `mv` command to rename your file or any directory, just simply write new name after you call the file or directory as an argument for command like example below

 ```structure
 mv <file_path or directory_path> <new_name>
 ```

 example

 ```
 mv /mnt/d/tt.md /mnt/d/textTile.md
 ```

 you can also path the file to new directory

 ### <a name="extra_03></a> using sed to modifiy text file without opening it

 it is crazy to know that there is a command like `sed` can edit file without opening it

 it is easy and straitforward you just need to know somethings like

 option `-i` or *in place* options means save your changes in the place of saving it

 ```
 sed -i "s/current_text/new_text/" <name_of_file_to_be_modified>
 ```
 for example i want to change `hello world` to another thing

 just write

 ```
 sed -i "s/hello world/greeting world/" talking.md
 ```

 ### <a name="extra_04"></a> what is sudo and why we need it

 sudo means superuser do

 as you already know or maybe you don't, Linux and other Linux distros are so secure 
it means you can't do anything you want whenever you want

 for example, you can't edit or modify any file inside root directories because you need a superpower to order to the machine

 and also everyone who sits front of the machine is not the owner for Linux operation system so if you are a real user, you need to use sudo to perform your order due to this action Linux always ask you to type machine's password to ensure that you are the real user of this machine
 but without sudo you can't even perform your actions because you are not the user or you're not permitted to do such a thing

 for example i can't create directory inside `/etc/` directory, to do this you need to put sudo at the first of command to perform an action you want

 ```
 wrong

 mkdir /etc/garbage

 correct 

 sudo mkdir /etc/garbage
 ```

 ### what is `!!` ?

 just imagine you were commanding your machine to create a directory but you forgot to put `sudo` at the beginning of your command and then you hit enter and terminal gives an error of incomplete action

so, you need to write your command once again but this time you write sudo first

but imagine if you could write `sudo` or any command at first and then just hit `!` sign twice to join your previous command to forgotten command part

yes, you can bring back your previous command and join it to another command you want

for example 

```
mkdir /mnt/version

error: you can't perform this action: permission denied

sudo !!

sudo mkdir /mnt/version

sed -i "s/new/old/"

error

!! config.md

sed -i "s/new/old/" config.md
```

### what is *alias*

alias is way to create shortcut keywords fro any command you want

1- find your `zshrc` file or `bashrc` file 
2- then open proper file in editor
3- at the end of the document simply write 
```
alias "custom keyword=command you want to make alias"

for example

alias "file=explorer.exe"

it means whenever i type file means explorer.exe command
```
4- after creating alias save your file and restart `zshrc` or `bashrc` file

alias "termux-clipboard-set=clip"

whenever i type `clip` in termux terminal means `termux-clipboard-set` command