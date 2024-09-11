# Table of Contents
1. [Linux File System](#linux-file-system)
2. [Common Linux Commands](#common-linux-commands)
    - [Vim Shortcuts](#vim-shortcuts)
3. [Command Categories](#command-categories)
    - [Archiving and Compression Commands](#archiving-and-compression-commands)
    - [File Viewing and Editing Commands](#file-viewing-and-editing-commands)
    - [File and Directory Management Commands](#file-and-directory-management-commands)
    - [Navigation Commands](#navigation-commands)
    - [Networking and Remote Management Commands](#networking-and-remote-management-commands)
    - [Permission and Ownership Commands](#permission-and-ownership-commands)
    - [Process Management Commands](#process-management-commands)
    - [System Information and Monitoring Commands](#system-information-and-monitoring-commands)
    - [User and Group Management Commands](#user-and-group-management-commands)
4. [Environment Variables](#environment-variables)
5. [What is Linux?](#what-is-linux)
6. [Setting Up Linux on Your Computer](#setting-up-linux-on-your-computer)
    - [Benefits of Virtualization](#benefits-of-virtualization)
7. [What Are Linux Distributions?](#what-are-linux-distributions)
8. [Linux Terminal](#linux-terminal)
9. [Linux Shortcuts](#linux-shortcuts)
10. [File Permissions](#file-permissions)

# Linux Notes

## Linux File System

Each directory in the Linux file system has a specific purpose, helping the system stay organized and efficient:

- **`/`**: The root of the file system.
- **`/home`**: Where user files are stored.
- **`/bin`, `/sbin`, `/usr/bin`**: Where executable programs are stored.
- **`/etc`**: Configuration files.
- **`/tmp`**: Temporary files.
- **`/var`**: Variable files like logs and caches.
- **`/lib`, `/usr/lib`**: Essential shared libraries and kernel modules.
- **`/boot`**: Contains boot loader files, including the kernel.
- **`/dev`**: Device files representing hardware devices.
- **`/proc`**: Virtual filesystem providing process and kernel information.
- **`/sys`**: Virtual filesystem with information about the system and kernel.
- **`/mnt`**: Mount point for temporarily mounted filesystems.
- **`/media`**: Mount point for removable media like CDs and USB drives.
- **`/root`**: Home directory for the root user.
- **`/opt`**: Optional application software packages.
- **`/srv`**: Data for services provided by the system (e.g., web servers).
- **`/run`**: Runtime data (e.g., system information since the last boot).

# Common Linux Commands

- **`mkdir`**: Create a new directory.
- **`rmdir`**: Delete directories.
- **`rm -r`**: Remove directories and their contents.
- **`ls`**: View the content of a directory.
- **`mv`**: Move files.
- **`locate`**: Search for files.
- **`cp`**: Copy files from one directory to another.
- **`head`**: View the first 10 lines of a file. You can specify the number of lines with the `-n` option (e.g., `head -n 5 file.txt`).
- **`tail`**: View the last 10 lines of a file. You can also specify the number of lines with the `-n` option (e.g., `tail -n 5 file.txt`).
- **`cat`**: Concatenate and display file content.
- **`touch`**: Create a new empty file.
- **`echo`**: Display text or variables.
- **`vim`**: Open and edit files using Vim text editor.

### Vim Shortcuts
- `:q`: Quit Vim.
- `:wq`: Save and quit.
- `yy`: Copy a line.
- `p`: Paste copied text.
- `/"search"`: Search for a term.
- `n` or `N`: Navigate through search results.
- `:set (no) number`: Show or hide line numbers.
- `:syntax on`: Enable syntax highlighting.
- `:w`: Save without quitting.

## Command Categories

### Archiving and Compression Commands

- **`tar`**: Archive files into a `.tar` file (can also compress):
  ```bash
  tar -cvf archive.tar file1 file2
  tar -xvf archive.tar
  ```
- **`gzip`**: Compress files using gzip:
  ```bash
  gzip file.txt
  gunzip file.txt.gz
  ```
- **`zip`**: Compress files into a `.zip` file:
  ```bash
  zip archive.zip file1 file2
  unzip archive.zip
  ```

### File Viewing and Editing Commands

- **`cat`**: View file content:
  ```bash
  cat filename.txt
  ```
- **`less`**: View file content with pagination:
  ```bash
  less filename.txt
  ```
- **`vim`**: Edit files using Vim:
  ```bash
  vim filename.txt
  ```
- **`nano`**: Edit files using Nano:
  ```bash
  nano filename.txt
  ```
- **`head`**: View the first 10 lines of a file:
  ```bash
  head filename.txt
  ```
- **`tail`**: View the last 10 lines of a file:
  ```bash
  tail filename.txt
  ```

### File and Directory Management Commands

- **`mkdir`**: Create a new directory:
  ```bash
  mkdir new_directory
  ```
- **`rm`**: Delete a file:
  ```bash
  rm filename.txt
  ```
- **`rmdir`**: Delete an empty directory:
  ```bash
  rmdir directory_name
  ```
- **`mv`**: Move or rename files and directories:
  ```bash
  mv file1.txt new_location/
  mv oldname.txt newname.txt
  ```
- **`cp`**: Copy files:
  ```bash
  cp file.txt new_location/
  ```

### Navigation Commands

- **`pwd`**: Show the current directory path:
  ```bash
  pwd
  ```
- **`cd`**: Change the current directory:
  ```bash
  cd /path/to/directory
  ```
- **`ls`**: List the contents of a directory:
  ```bash
  ls
  ls -l  # detailed list
  ```
- **`find`**: Search for files and directories:
  ```bash
  find /path -name filename.txt
  ```

### Networking and Remote Management Commands

- **`ping`**: Check the network connectivity to a host:
  ```bash
  ping google.com
  ```
- **`ifconfig`**: Display or configure network interfaces (use `ip` in newer systems):
  ```bash
  ifconfig
  ```
- **`ssh`**: Connect to a remote system via SSH:
  ```bash
  ssh user@hostname
  ```
- **`scp`**: Copy files between systems over SSH:
  ```bash
  scp localfile.txt user@remote:/path/to/remote
  ```

### Permission and Ownership Commands

- **`chmod`**: Change file permissions:
  ```bash
  chmod 755 filename.txt
  ```
- **`chown`**: Change the ownership of a file or directory:
  ```bash
  chown user:group filename.txt
  ```
- **`chgrp`**: Change the group ownership of a file:
  ```bash
  chgrp groupname filename.txt
  ```

### Process Management Commands

- **`ps`**: View running processes:
  ```bash
  ps aux
  ```
- **`top`**: Display real-time process information:
  ```bash
  top
  ```
- **`kill`**: Terminate a process by its PID:
  ```bash
  kill 1234
  ```
- **`killall`**: Kill all processes by name:
  ```bash
  killall processname
  ```

### System Information and Monitoring Commands

- **`df`**: Display disk space usage:
  ```bash
  df -h
  ```
- **`du`**: Show the disk usage of files and directories:
  ```bash
  du -sh *
  ```
- **`free`**: Show memory usage:
  ```bash
  free -h
  ```
- **`uptime`**: Show system uptime and load averages:
  ```bash
  uptime
  ```
- **`dmesg`**: Display kernel messages:
  ```bash
  dmesg
  ```

### User and Group Management Commands

- **`useradd`**: Add a new user:
  ```bash
  sudo useradd username
  ```
- **`passwd`**: Set or change a user’s password:
  ```bash
  sudo passwd username
  ```
- **`usermod`**: Modify a user's account:
  ```bash
  sudo usermod -aG groupname username
  ```
- **`deluser`**: Remove a user:
  ```bash
  sudo deluser username
  ```
- **`groupadd`**: Create a new group:
  ```bash
  sudo groupadd groupname
  ```

## Environment Variables

Common environment variables:
- **`$PATH`**: Directories where the shell looks for executable files.
- **`EDITOR`**: The default text editor.
- **`HOSTNAME`**: The name of the machine.
- **`LANG`**: Language and localization settings.
- **`PWD`**: Current working directory.
- **`UID`**: User ID.
- **`HOME`**: Home directory.

## What is Linux?

Linux is an open-source operating system that is the backbone of many servers, networks, and cloud infrastructures. Unlike proprietary systems like Windows or macOS, Linux allows anyone to study, modify, and redistribute its source code.

## Setting Up Linux on Your Computer

You can use virtualization to run Linux/Ubuntu on your current operating system. **VirtualBox** is a free tool that allows you to do this.

### Benefits of Virtualization:
- Run Linux without replacing your current OS.
- Run multiple operating systems on a single machine.
- Isolate different systems while sharing resources.

## What Are Linux Distributions?

A Linux distribution (distro) is a version of Linux designed for different use cases. Think of Linux as the **engine** and distributions as the **vehicle**.

**Ubuntu** is one of the most beginner-friendly distributions.

## Linux Terminal

The terminal is a command-line interface (CLI) that lets you interact with your operating system by typing commands. It provides direct control of your OS.

Common tasks include:
- Navigating the file system.
- Installing and configuring software.
- Performing administrative tasks.

## Linux Shortcuts

- **Open terminal**: `Ctrl + Alt + T`
- **Increase text size**: `Ctrl + Shift + +`
- **Clear the screen**: `Ctrl + L`
- **Exit typing mode**: `Ctrl + D`

## File Permissions

Linux uses binary, octal, and string representation for file permissions.

Use the **CHMOD Calculator** built by CoderCo to calculate permissions:
[CHMOD Calculator](https://chmod-calc-five.vercel.app/)