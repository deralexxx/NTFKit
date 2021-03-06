####change hostname
```
vi /etc/hostname
```

####change ssid
```
vi /etc/hostapd/hostapd.conf
```

####change ssh key
```
rm -v /etc/ssh/ssh_host_*
dpkg-reconfigure openssh-server
service ssh restart
```

####reboot
```
sync; sync; reboot
```

####install ufw
```
apt update
apt install ufw
```

####configure ufw
```
ufw allow ssh
ufw enable
```

####create ssh keys
```
su - ntfk
ssh-keygen -f ~/.ssh/id_rsa -t rsa -N "''"

source /etc/ntfk.conf
scp ~/.ssh/id_rsa.pub ntfk@$NTFK_MASTER:.ssh/`hostname`.id_rsa.pub

rm -Rf /mnt/sda1/SanDiskSecureAccess/
rm /mnt/sda1/RunSanDiskSecureAccess_Win.exe
rm /mnt/sda1/Back*
```

####install snort
```
apt install snort
```

####install yara
```
apt install yara
```

####install yara
```
apt install autossh
```

#### use raspi-config to disable GUI desktop
#### use raspi-config to disable GUI desktop
####raspi-config
#### --> 3 Boot Options
####   --> B1 Desktop / CLI
####     --> B1 Console
```
sudo raspi-config nonint do_boot_behaviour B1
```


#### when cloning an existing sensor, edit the following files after using DD to clone the microSD
#### /etc/hostname - change hostname
#### /etc/hostapd/hostapd.conf - change SSID
#### /etc/udev/rules.d/70-persistent-net.rules - modify to make onboard interfaces eth0 and wlan0
