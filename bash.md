# Bash Shell Scripting Cheet Sheet
## #!/bin/bash

-  [uname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#uname)
-  [hostname](https://github.com/naveenkumar0306/bash_shell_scripting/blob/main/bash.md#hostname)
-  

#### uname
```bash
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ uname -a     // Displays the system information of your Linux computer
Linux personalpc01.bash.com 3.10.0-1160.21.1.el7.x86_64 #1 SMP Mon Feb 22 18:03:13 EST 2021 x86_64 x86_64 x86_64 GNU/Linux
```
// Linux - Kernal Name
// personalpc01.bash.com - Hostnmae
// 3.10.0-1160.21.1.el7.x86_64 - Kernal Release
// 1 SMP Mon Feb 22 18:03:13 EST 2021 - Kernal Version
// x86_64 - hardware name
// x86_64 - Processor Type
// x86_64 - hardware platform
// GNU/Linux - Operating System


#### hostname
```bash
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ hostname       // Displays hostname of the system
personalpc01.bash.com
[naveen.kandhasamy@personalpc015 AKA pc-cbe01 ~]$ hostname -s   // Displays hostname of the system without domain
personalpc01
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ hostname -d    // Displays domain on which the system connected
bash.com
[naveen.kandhasamy@personalpc01 AKA pc-cbe01 ~]$ hostname -i    // Displays ipaddress of the system
10.226.143.170
```
