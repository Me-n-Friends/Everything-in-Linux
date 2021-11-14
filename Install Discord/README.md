# Install Discord
Tested on: `Kali Linux`
Kernel Version: `5.14.0-kali2-amd64`
Date created: `Sun 14 Nov 2021, 20:59`

This article is made for those who have problem installing Discord with Debian Package Method. I made this article from this [link](https://itsfoss.com/install-discord-linux/). All credit goes into [itsfoss.com](https://itsfoss.com/) </br>

---

## What are Discord?
---
Discord is a VoIP, instant messaging and collaboration app. It is a great software to run a community, for work, for gaming and many more. </br>

## Installing Discord via Debian Package Method
---
1. Go to the Discord download page from this [link](https://discord.com/download) and select `deb`
![Debian Method](https://imgur.com/81XQhhY.png)
2. Go to path where Discord is been downloaded
3. Run this command to install on your system
```
# apt install ./discord-0.0.16.deb
```
NB: change the version number according to the latest version </br>

## Installing Discord via Tar
---
1. Go to the Discord download page from this [link](https://discord.com/download) and select `tar.gz`
![Debian Method](https://imgur.com/81XQhhY.png)
2. Go to path where Discord is been downloaded
3. Extract the package to `/opt` directory by running this command
```
# tar -xvzf discord-0.0.16.tar.gz -C /opt
```
4. Create a symbolic link to binary file in `/usr/bin` directory
```
# ln -sf /opt/Discord/Discord /usr/bin/discord
```
5. Run Discord and enjoy