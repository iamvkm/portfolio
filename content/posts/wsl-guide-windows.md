---
title: "How to install Kali Linux on Windows 10 through WSL"
date: 2020-09-13T19:49:57+05:30
draft: false
---

The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a traditional virtual machine or dual-boot setup.

### Installing WSL

Before we get started, update your machine. You need to be running on Windows 10 version 1903 build 18362 or higher.

#### Method I - Using GUI

Search for Windows Features in and check the Windows Subsystem for Linux and Virtual Machine Platform.

![Windows Features](https://www.linkpicture.com/q/Screenshot-103.png)

Restart your machine.

#### Method II - Using Powershell

Open power shell in administrator and type the following...

`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`
this will enable Windows Subsystem for Linux and restart the machine

`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`
this will enable Virtual Machine Platform and restart the machine

`wsl --set-default-version 2`
this will set wsl 2 as your default version

### Installing Kali

Install Kali from the [Microsoft Store](https://aka.ms/wslstore), download and install it.
Open the Kali system from the start menu.
Add a new user and set up the password...

![Kali on Windows 10](https://www.linkpicture.com/q/Screenshot-108.png)

You are halfway there, you have successfully installed kali using WSL.

### Configuring Kali (Setting up a GUI)

Now let us Install the Desktop Environment (win-kex)
Open kali terminal and run the commands

`sudo apt update`
To update the kali repositories

`sudo apt upgrade`
To install the updates available for kali

`sudo apt install kali-win-kex`
To install the win-kex (Kali Desktop Experience for Windows)

Note: If you get error while installing `kali-win-kex` then make sure you have enabled `Virtual Machine Platform` and are using Kali in WSL2 and not WSL1.

![Trubleshoot](https://www.linkpicture.com/q/Screenshot-135.png)

Also, you can press F8 key to open VNC options and exit full screen!

You are Done! That is it, you are all set.

![Kali on windows 10](https://www.linkpicture.com/q/Screenshot-130.png)

If you want to install the complete kali by running the command, this is 'optional' and you can do it if you have space.
`sudo apt install kali-linux-large`
