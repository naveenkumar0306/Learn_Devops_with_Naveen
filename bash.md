# Learn Bash Shell Scripting
## #!/bin/bash

-  [File_system_hierarchy](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#File_system_hierarchy)
-  [ls](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#ls)
-  [uname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#uname)
    - [Print_the_system_information_of_your_Linux_computer](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Print_the_system_information_of_your_Linux_computer)
-  [hostname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#hostname)
    - [Print_hostname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Print_hostname)
    - [Print_ipaddress](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Print_ipaddress)
-  [Environment_Variable](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Environment_Variable)
    - [print_list_of_environment_variables](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#print_list_of_environment_variables)
    - [set_unset_environment_variable](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#set_unset_environment_variable)
    - [Persisting_Environment_Variables_for_a_User](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Persisting_Environment_Variables_for_a_User)

### File_system_hierarchy
```
/bin        // Contains the system Binaries
/home       // Contains user’s Home directory
/dev        // Device files like block and character devices
/etc        // System Configuration
/lib        // Shared library and kernel modules
/lib64      // Contains 64-bit version shared library
/var        // Data which varies over time
/sbin       // Binary utilities for which only root or system administrator has access
/mnt        // Mount point for a filesystem
/tmp        // Used for storing temporary data and files
/proc       // Kernel data structure mounted as filesystem. Only applicable to Linux based OS
/boot       // Contains the initramfs and kernel image.
/sys        //Kernel data structure for different hardware and device like Block Device, Firmware, ACPI etc. Applicable for Linux based OS only.
```

### ls
```
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 /]$ ls                     // List files and folders in the current directory
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

[naveen.kandhasamy@personalpc01 AKA pc-cbe01 /]$ ls /var/               // List files and folders in the /var directory
adm    crash  empty  gopher    lib    lock  mail  nis  ossec     run    tmp

[naveen.kandhasamy@personalpc01 AKA pc-cbe01 /]$ ls -la                 // Long listing files and folders in the current directory including hidden files
total 540
dr-xr-xr-x.   17 root root    244 Apr  7  2021 .
dr-xr-xr-x.   17 root root    244 Apr  7  2021 ..
-rw-r--r--     1 root root      0 Apr  7  2021 .autorelabel
lrwxrwxrwx.    1 root root      7 Apr  7  2021 bin -> usr/bin
dr-xr-xr-x.    5 root root   4096 May 12 03:23 boot

[naveen.kandhasamy@personalpc01 AKA pc-cbe01 /]$ ls -lia                // Long listing files and folders in the current directory including hidden files with inode value
total 540
     64 dr-xr-xr-x.   17 root root    244 Apr  7  2021 .
     64 dr-xr-xr-x.   17 root root    244 Apr  7  2021 ..
 334358 -rw-r--r--     1 root root      0 Apr  7  2021 .autorelabel
    109 lrwxrwxrwx.    1 root root      7 Apr  7  2021 bin -> usr/bin

[naveen.kandhasamy@personalpc01 AKA pc-cbe01 /]$ ls -lrth               // Long listing files and folders in the current directory by reverse sorting last modified files with human readable file size(4.0k - reads 4killobytes)
total 540K
drwxr-xr-x.    2 root root    6 Dec 14  2017 srv
drwxr-xr-x.    2 root root    6 Dec 14  2017 mnt
drwxr-xr-x.    2 root root    6 Dec 14  2017 media
lrwxrwxrwx.    1 root root    7 Apr  7  2021 bin -> usr/bin
lrwxrwxrwx.    1 root root    9 Apr  7  2021 lib64 -> usr/lib64
lrwxrwxrwx.    1 root root    7 Apr  7  2021 lib -> usr/lib
lrwxrwxrwx.    1 root root    8 Apr  7  2021 sbin -> usr/sbin
drwxr-xr-x.   13 root root  155 Apr  7  2021 usr
drwxr-xr-x.   21 root root 4.0K Apr 15  2021 var
```

### uname
#### Print_the_system_information_of_your_Linux_computer
```
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ uname -a     
Linux personalpc01.bash.com 3.10.0-1160.21.1.el7.x86_64 #1 SMP Mon Feb 22 18:03:13 EST 2021 x86_64 x86_64 x86_64 GNU/Linux
```
```
// Linux - Kernal Name
// personalpc01.bash.com - Hostname
// 3.10.0-1160.21.1.el7.x86_64 - Kernal Release
// 1 SMP Mon Feb 22 18:03:13 EST 2021 - Kernal Version
// x86_64 - hardware name
// x86_64 - Processor Type
// x86_64 - hardware platform
// GNU/Linux - Operating System
```

### hostname
#### Print_hostname
```
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ hostname       
personalpc01.bash.com
```
#### Print_ipaddress
```
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ hostname -i
10.226.143.170
```

### Environment_Variable
#### print_list_of_environment_variables
```
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ env
MANPATH=:/opt/puppetlabs/puppet/share/man
XDG_SESSION_ID=13337
HOSTNAME=personalpc01.bash.com
TERM=xterm
SHELL=/bin/bash
HISTSIZE=1000
SSH_CLIENT=10.232.83.0 6037 22
SSH_TTY=/dev/pts/0
USER=naveen.kandhasamy
LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=01;05;37;41:su=37;41:sg=30;43:ca=30;41:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arc=01;31:*.arj=01;31:*.taz=01;31:*.lha=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.tlz=01;31:*.txz=01;31:*.tzo=01;31:*.t7z=01;31:*.zip=01;31:*.z=01;31:*.Z=01;31:*.dz=01;31:
MAIL=/var/spool/mail/naveen.kandhasamy
PATH=/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/opt/puppetlabs/bin:/home/naveen.kandhasamy/.local/bin:/home/naveen.kandhasamy/bin
PWD=/home/naveen.kandhasamy
LANG=en_US.UTF-8
HISTCONTROL=ignoredups
KRB5CCNAME=FILE:/tmp/krb5cc_1157651176_6B4YUj
SHLVL=1
HOME=/home/naveen.kandhasamy
LOGNAME=naveen.kandhasamy
SSH_CONNECTION=10.232.83.0 6037 10.226.143.170 22
LESSOPEN=||/usr/bin/lesspipe.sh %s
XDG_RUNTIME_DIR=/run/user/1157651176
HISTTIMEFORMAT=%m/%d/%y %T
_=/usr/bin/env
```

#### set_unset_environment_variable
```
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ export JAVA_HOME=/opt/bt/java/jdk1.8.0_311-x86_64        // set JAVA_HOME environment varaiable
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ echo $JAVA_HOME                                          // print JAVA_HOME environment varaiable
/opt/bt/java/jdk1.8.0_311-x86_64
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ unset JAVA_HOME                                          // unset JAVA_HOME environment varaiable - echo $JAVA_HOME will return empty since JAVA_HOME varaible is removed   
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ echo $PATH                                               // print PATH environment varaiable
PATH=/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/opt/puppetlabs/bin:/home/naveen.kandhasamy/.local/bin:/home/naveen.kandhasamy/bin
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ export PATH=$PATH:/opt/bt/java/jdk1.8.0_311-x86_64/bin/  // append JAVA bin path to the PATH varaiable
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ echo $PATH                                               // print updated PATH environment varaiable(/opt/bt/java/jdk1.8.0_311-x86_64/bin/ is appended to the PATH varaible)
PATH=/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/opt/puppetlabs/bin:/home/naveen.kandhasamy/.local/bin:/home/naveen.kandhasamy/bin:/opt/bt/java/jdk1.8.0_311-x86_64/bin/
```

#### Persisting_Environment_Variables_for_a_User
```
// When an environment variable is set from the shell using the export command, its existence ends when the user’s sessions ends. This is problematic when we need the variable to persist across sessions. To make an environment persistent for a user’s environment, we export the variable from the user’s profile script.

[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ vi ~/.bash_profile               // Open the current user’s profile into a text editor
export JAVA_HOME=/opt/bt/java/jdk1.8.0_311-x86_64                                   // Add the export command for every environment variable you want to persist and save changes.
// Adding the environment variable to a user’s bash profile alone will not export it automatically. However, the variable will be exported the next time the user logs in
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 bin]$ source ~/.bash_profile           // To immediately apply all changes to bash_profile
```


