# Snap Guide for Beginner
Tested on: `Kali Linux`
Kernel Version: `5.14.0-kali2-amd64`
Date created: `Sun 14 Nov 2021, 20:28`

This article I made was taken from a cool article to installing Snap in your linux distribution. You can check the article for more detail information in this [link](https://www.tecmint.com/install-snap-in-linux/) </br>

I just rewrite and modify a little it to keep a note for myself and for community. All credit goes to [tecmint.com](https://www.tecmint.com/) </br>

---

## What are Snap Packages?
---
Snaps are X-Distribution, dependency-free, and easy to install applications packaged with all their dependencies to run on all major Linux distributions. From a single build, a Snap will run on all supported Linux distributions on desktop, in the cloud, and IoT. Supported distributions include Ubuntu, Debian, Fedora, Arch-Linux, Manajro, and CentOS/RHEL. </br>

The main components of the Snap package management system are:
- **snapd** – the background service that manages and maintains your snaps on a Linux system.
- **snap** – both the application package format and the command-line interface tool used to install and remove snaps and do many other things in the snap ecosystem.
- **snapcraft** – the framework and powerful command-line tool for building snaps.
- **snap store** – a place where developers can share their snaps and Linux users search and install them.

## Installing Snapd in Linux
---
To install **snapd** package on your system, run the appropriate command for your linux distribution.

```
---On Debian and Ubuntu---

# apt install snapd
# apt update

---On Fedora Linux---

# dnf install snapd

---On CentOS and RHEL---

# yum install epel-release
# yum install snapd

---On OpenSUSE - replace openSUSE_Leap_15.0 with the version---

# zypper addrepo --refresh https://download.opensuse.org/repositories/system:/snappy/**openSUSE_Leap_15.0** snappy
# zypper --gpg-auto-import-keys refresh
# zypper dup --from snappy
# zypper install snapd

---On Manjaro Linux---
# pacman -S snapd

---On Arch Linux---
# git clone https://aur.archlinux.org/snapd.git
# cd snapd
# makepkg -si
```

After installing **snapd** on your system, enable the `systemd` unit that manages the main Snap communication socket, using the `systemctl` commands as follows:
```
# systemctl enable --now snapd.socket
# systemctl enable --now apparmor.service
```
NB: Snap can't run if `snapd.socket` is not running </br>
Make sure to check it by running this command:
```
# systemctl is-active snapd.socket
# systemctl status snapd.socket
# systemctl is-enabled snapd.socket
```
![Check Snapd Service Status](https://www.tecmint.com/wp-content/uploads/2020/06/check-if-snapd-socket-is-running.png)
</br>
Next, enable **classic snap** support by creating a symbolic link between `/var/lib/snapd/snap` and `/snap` as follows:
```
# ln -s /var/lib/snapd/snap /snap
```

To check the version of snapd and snap command-line tool installed on your system, run the following command:
```
$ snap version
```
![Check Snapd and Snap Version](https://www.tecmint.com/wp-content/uploads/2020/06/check-snapd-and-snap-version.png)

## Install Applications in Snap
---
You can install an applications via Snap using this command:
```
# snap install <applications_name>
```

## Running Applications in Snap
---
To run the applications you have installed, run this command as follows:
```
# snap run <applications_name>
```

## Uninstall Applications in Snap
---
To uninstall the applications, simply type this command in your terminal:
```
# snap remove <applications_name>
```