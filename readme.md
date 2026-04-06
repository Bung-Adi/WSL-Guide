# WSL Guide

jumpt to :  
[1. Why](#1-why-you-should-use-WSL)  
[2. What to setup](#2-make-sure-device-and-windows-os-ready)  
[3. Install Base](#3-install-the-base)  
[4. Basic](#4-basic-command)  
[5. Whats Next](#5-Whats-Next)

___  
### 1 why you should use WSL  
For some people many things need or better to do in linux but  dualboot is feel to much especially diskspace things.
In my case I use WSL for Docker and OpenCode for now.
but maybe will be usefull for other things too in the future.  

___  
### 2 Make sure device and windows OS ready
The First thing first preparation to use WSL (Windows sub-sistem linux) make sure your Windows device ready 

- check your Task Manager > Performance > CPU. If its say *Virtualization* : disable.  
* Restart or Shutdown first then go to your device boot menu to enable it.  
* To get into boot menu you can check your motherboard or laptop manual. If you are on laptop you can visit [mobilespecs.net](https://mobilespecs.net/laptop/) and search your laptop model  
* Find the Setting: Look for a menu called "Advanced," "CPU Configuration," or "Security."
1. If you have an Intel CPU: Look for Intel Virtualization Technology (VT-x).
1. If you have an AMD CPU: Look for SVM Mode.
* Enable it Save end Exit boot menu.  

- when you back to your Windows  
In the search bar search "Turn Windows features on or off" and make sure these are checked :  
1. Virtual Machine Platform
2. Virtual Machine Platform  
- then you might need to restart again

___  
### 3. Install the base

#### I install Debian  
for WSL to work you need to install base Linux Os Distro. In my case I install Debian.  
`wsl --install -d Debian`  
to use these Debian WSL.  
just type `wsl` in command prompt  
    
___  
### 4. basic command

##### to detect whats installed  
`wsl --list --verbose`

##### set version WSL  
`wsl --set-version <distribution name> <versionNumber>`
or  
`wsl --set-default-version <Version>`

##### update
`wsl --update`

##### status
`wsl --status`

##### shutdown
`wsl --shutdown`

#####
`wsl --help`

___  
### 5 Whats Next
- [Docker on WSL](Docker/index-docker.md)