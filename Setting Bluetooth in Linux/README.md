# Setting up Bluetooth Connection in Linux

[Reference](https://computingforgeeks.com/connect-to-bluetooth-device-from-linux-terminal/)

---

## Step 1: Installing package and dependencies
Open terminal and type `sudo apt-get -y install bluetooth bluez bluez-tools rfkill` and press enter. This installation provides the `bluetoothctl` utility. </br>

## Step 2: Check the bluetooth device is enable or not
To check the bluetooth device is enable, we run this command `systemctl is-enabled bluetooth.service` </br>

## Step 3: Pairing to Bluetooth device
Check the bluetooth service is blocked or not with `rfkill` </br>
To unblock the service, type `rfkill unblock bluetooth` and check once again to make sure the service is unblock </br>
Now type `bluetoothctl` to enter the bluetooth device interface </br>
```
[bluetooth]# agent KeyboardOnly
[bluetooth]# default-agent
[bluetooth]# power on
[bluetooth]# scan on
[bluetooth]# pair <MAC Address>
[bluetooth]# trust <MAC Address>
[bluetooth]# paired-devices
[bluetooth]# devices
```
## Step 4: Connecting to paired devices
```
[bluetooth]# connect <MAC Address>
[bluetooth]# info
```
