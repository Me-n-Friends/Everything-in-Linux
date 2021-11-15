# Install Anaconda in Linux
Tested on: `Kali Linux`
Kernel Version: `5.14.0-kali2-amd64`
Date created: `Mon 15 Nov 2021, 08:19`

Anaconda is a distribution of the Python and R programming language for scientific computing that aims to simplify package management and deployment. The distribution includes data-science packages suitable for Windows, Linux, and macOS. For more detail article, you can visit this [link](https://docs.anaconda.com/anaconda/install/linux/)

## Prerequisites
---
```
---Debian---

# apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
```

## Installation
---
1. Download [Anaconda Installer for Linux](https://www.anaconda.com/products/individual#linux)
2. Run the following to install Anaconda
```
$ bash /path/to/download/anaconda
```
3. The installer prompts “In order to continue the installation process, please review the license agreement.” Click Enter to view license terms.
4. Scroll to the bottom of the license terms and enter “Yes” to agree.
5. The installer prompts you to click Enter to accept the default install location, CTRL-C to cancel the installation, or specify an alternate installation directory. If you accept the default install location, the installer displays ``“PREFIX=/home/\<user\>/anaconda\<2 or 3\>”`` and continues the installation. It may take a few minutes to complete.
6. The installer prompts “Do you wish the installer to initialize Anaconda3 by running conda init?” We recommend “yes”.
7. The installer finishes and displays “Thank you for installing Anaconda\<2 or 3\>!”
8. Reload your terminal by typing `source ~/.bashrc` or close and reopen the terminal for the installation to take effect.
9. To control whether or not each shell session has the base environment activated or not, run `conda config --set auto_activate_base False or True`. To run conda from anywhere without having the base environment activated by default, use `conda config --set auto_activate_base False`. This only works if you have run `conda init` first.

## Install Anaconda Navigator
---
1. Run this command in terminal
```
$ conda install anaconda-navigator
```
2. Follow along the installation
3. After the installation is complete, you can run anaconda-navigator by running `conda run anaconda-navigator`