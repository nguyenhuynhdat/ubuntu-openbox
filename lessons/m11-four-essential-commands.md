---
layout: default
title: FOUR ESSENTIAL COMMANDS
description: learn about APT and apt-get.
---

## Goal of this lesson:

Although you may have enough experience with command-line, to be familiar with these fours commands are very important for this course.

They are:
```
$ apt-get update
$ apt-get upgrade
$ apt-get install/ remove
$ nano
```
This may be the most boring chapter of this series, but it is kind of the most important one. Please try to go through it!

### What is Command-line:

A command is text which is written in a specific syntax. After entering a command into any terminal, the shell of your OS can understand and interpret this syntax and pass it to the OS to do what you want.

Some command only available for power user, and you need the command sudo before it. It also may ask you to confirm root power if needed.

Why do we use command line a lot in this courses? Because we are building our operating system from the ground up. Most of the time we will not have the luxury of GUI.

Moreover, relying on GUI is not a healthy attitude in my opinion, command line actually is a powerful tool that will help you on every aspect of Linux.

### Apt and the source.list file:

>Apt (short for Advanced Package Tool) is a set of core tools inside Debian. Apt makes it possible to:

>Install applications

>Remove applications

>Keep your applications up to date

>And much more...

>Apt, which basically resolves dependency problems and retrieves the requested packages.

*(from Debian wiki)*

Apt frees you from the madness of specifying each of dependencies when installing an application. In an Linux OS, various applications may simultaneously need the same dependencies. Apt will keep the harmony between them by specifying only the appropriate version.
```
/etc/apt/source.list
```
This file is listing the sources where packages are being stored so that apt can know where to obtained them. These sources are called **repositories**.

### The four commands:

1. Update repositories
```
sudo apt-get update
```
This is the most important commands of apt-get.
What it does is to go to the addresses listed in the **/apt/etc/source.list** file and update what have been changed from the last time you update repositories (which packages are on there now and which are the latest versions of them).
After that **apt** will have the newest information of repositories (sources of packages) and can ask for the right version of packages. Otherwise, error will occur as the version of the package asked (old info) is not matching with that of is on repositories.

2. Install a package
```
sudo apt-get install firefox
```
This command will also update the firefox package if it has been already installed.

3. Remove a package
```
sudo apt-get remove firefox
```
To also remove all of firefox's configuration files on your system add the flag **--purge**:
```
sudo apt-get remove --purge firefox
```

4. Edit text file using Nano editor
**Nano** lets you edit text file directly from the terminal. In a Linux system, configuration files are text files.
To edit a text:
```
sudo nano /directory/configuration_file
```
Please use the navigation keys (up/ down/ left/ right arrows) to navigate through the file and edit it.
After making the changes, **Ctrl + X** to close nano editor, it will ask you to save, type **“Y”** to confirm, or type **"N"** to abort.
