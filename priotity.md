nice is a subshell

    nice: ‘20’: No such file or directory
    nick@nick-VirtualBox:~$ nice -n -20 bash
    nice: cannot set niceness: Permission denied
    nick@nick-VirtualBox:~$ nice
    0
    nick@nick-VirtualBox:~$ exit
    exit
    nick@nick-VirtualBox:~$ sudo nice -n -20 bash
    [sudo] password for nick: 
    root@nick-VirtualBox:~# nice
    -20
    root@nick-VirtualBox:~# exit
    exit
    nick@nick-VirtualBox:~$ nice
    0

renice - change process priority

    nick@nick-VirtualBox:~$ echo $$
    1459
    nick@nick-VirtualBox:~$ sudo renice --pid 1459 -n -20
    renice: invalid priorty '--pid'
    Try 'renice --help' for more information.
    nick@nick-VirtualBox:~$ sudo renice -n -20 --pid 1459
    1459 (process ID) old priority 0, new priority -20
    nick@nick-VirtualBox:~$ nice
    -20
