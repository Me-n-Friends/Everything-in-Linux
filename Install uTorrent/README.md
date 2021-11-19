# Install uTorrent
Tested on: `Kali Linux`
Kernel Version: `5.14.0-kali4-amd64`
Date created: `Fri 19 Nov 2021, 12:27`

Reference of this article is belong to [bettertechtips.com](https://www.bettertechtips.com/linux/install-utorrent-linux/) </br>

## Install uTorrent
---
```
$ sudo apt install libssl1.0.0 libssl-dev
$ sudo tar xvf utserver.tar.gz -C /opt
$ sudo ln -s /opt/utorrent-server-alpha-v3_3/utserver /usr/bin/utserver
$ utserver -settingspath /opt/utorrent-server-alpha-v3_3/ &
```
Now open web browser and type `127.0.0.1:8080/gui` </br>
There you'll be asked to enter username and password. Input the username as `admin` and leave the password column as blank.