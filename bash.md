# Learn Bash Shell Scripting
## #!/bin/bash

-  [uname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#uname)
    -  [Print_the_system_information_of_your_Linux_computer](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Print_the_system_information_of_your_Linux_computer)
-  [hostname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#hostname)
    - [Print_hostname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Print_hostname)
    - [Print_ipaddress](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Print_ipaddress)
-  [Environment_Variable](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#Environment_Variable)
    - [print_list_of_environment_variables](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#print_list_of_environment_variables)
    - [set_unset_environment_variable](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#set_unset_environment_variable)

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
