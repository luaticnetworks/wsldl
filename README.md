# wsldl
General Purpose WSL Distribution Installer & Launcher


![screenshot](https://raw.githubusercontent.com/wiki/yuk7/wsldl/img/Arch_Alpine_Cent.png)

[![Travis (.org)](https://img.shields.io/travis/yuk7/wsldl.svg?logo=Travis&style=flat-square)](https://travis-ci.org/yuk7/wsldl)
[![AppVeyor](https://img.shields.io/appveyor/ci/yuk7/wsldl.svg?logo=AppVeyor&style=flat-square)](https://ci.appveyor.com/project/yuk7/wsldl)
[![Github All Releases](https://img.shields.io/github/downloads/yuk7/wsldl/total.svg?style=flat-square)](https://github.com/yuk7/wsldl/releases/latest)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
![License](https://img.shields.io/github/license/yuk7/wsldl.svg?style=flat-square)



## 💻Requirements
* Windows 10 1709 Fall Creators Update 64bit or later.
* Windows Subsystem for Linux feature is enabled.

## 📦Install with prebuilt rootfs
#### 1. Download installer zip
[Alpine Linux](https://github.com/yuk7/AlpineWSL)

[Alpine Linux with Git-LFS and Sphinx](https://github.com/binarylandscapes/AlpineWSL) (by [binarylandscapes](https://github.com/binarylandscapes))

[Amazon Linux 2](https://github.com/yosukes-dev/AmazonWSL) (by [yosukes-dev](https://github.com/yosukes-dev))

[Arch Linux](https://github.com/yuk7/ArchWSL)

[Artix Linux](https://github.com/hdk5/ArtixWSL) (by [hdk5](https://github.com/hdk5))

[CentOS](https://github.com/yuk7/CentWSL)

[CentOS](https://github.com/fbigun/WSL-Distro-Rootfs) (by [fbigun](https://github.com/fbigun))

[Clear Linux](https://github.com/wight554/ClearWSL/) (by [wight554](https://github.com/wight554))

[Fedora](https://github.com/yosukes-dev/FedoraWSL) (by [yosukes-dev](https://github.com/yosukes-dev))

[Red hat(UBI)](https://github.com/yosukes-dev/RHWSL) (by [yosukes-dev](https://github.com/yosukes-dev))

[Void Linux (glibc)](https://github.com/am11/VoidWSL) (by [am11](https://github.com/am11))

[Void Linux (musl-libc)](https://github.com/am11/VoidMuslWSL) (by [am11](https://github.com/am11))

#### 2. Extract all files in zip file to same directory

#### 3.Run exe to Extract rootfs and Register to WSL
Exe filename is using to the instance name to register.
If you rename it, you can register with a different name.


## 🔧Install with any rootfs
#### 1. [Download Launcher.exe](https://github.com/yuk7/wsldl/releases/latest)
#### 2. Rename it for distribution name to register.
(Ex:Rename to Arch.exe if you want to use "Arch" for the Instance name)
#### 3. Put your rootfs.tar.gz in same directory as exe (Installation directory)
#### 4. Run exe to install. This process may take a few minutes.

Note: You can distribute your distribution including wsldl exe.

## 📝How-to-Use(for Installed Instance)
#### exe Usage
```cmd
Usage :
    <no args>
      - Open a new shell with your default settings.

    run <command line>
      - Run the given command line in that distro. Inherit current directory.

    runp <command line (includes windows path)>
      - Run the path translated command line in that distro.

    config [setting [value]]
      - `--default-user <user>`: Set the default user for this distro to <user>
      - `--default-uid <uid>`: Set the default user uid for this distro to <uid>
      - `--append-path <on|off>`: Switch of Append Windows PATH to $PATH
      - `--mount-drive <on|off>`: Switch of Mount drives

    get [setting]
      - `--default-uid`: Get the default user uid in this distro
      - `--append-path`: Get on/off status of Append Windows PATH to $PATH
      - `--mount-drive`: Get on/off status of Mount drives
      - `--lxguid`: Get WSL GUID key for this distro

    backup [contents]
      - `--tgz`: Output backup.tar.gz to the current directory using tar command
      - `--reg`: Output settings registry file to the current directory

    clean
      - Uninstall the distro.

    help
      - Print this usage message.
```


#### Just Run exe
```cmd
>{InstanceName}.exe
[root@PC-NAME user]#
```

#### Run with command line
```cmd
>{InstanceName}.exe run uname -r
4.4.0-43-Microsoft
```

#### Run with command line with path translation
```cmd
>{InstanceName}.exe runp echo C:\Windows\System32\cmd.exe
/mnt/c/Windows/System32/cmd.exe
```

#### Change Default User(id command required)
```cmd
>{InstanceName}.exe config --default-user user

>{InstanceName}.exe
[user@PC-NAME dir]$
```

#### How to uninstall instance
```cmd
>{InstanceName}.exe clean

```

## 🛠How-to-Build
Please see [DEVELOPERS.md](https://github.com/yuk7/wsldl/blob/master/DEVELOPERS.md)

## 📄License
[MIT](https://github.com/yuk7/wsldl/blob/master/LICENSES.md)

Copyright (c) 2017-2020 yuk7
