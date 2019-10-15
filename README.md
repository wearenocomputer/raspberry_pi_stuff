# raspberry_pi_stuff-
Useful commands for Raspberry Pi

//autostart nodejs service

sudo nano /etc/rc.local

//kill node process

sudo pkill node

//set fix ip address
sudo nano /etc/dhcpcd.conf
::interface eth0
::static ip_address=192.168.1.3/24
::static routers=192.168.1.1
::static domain_name_servers=192.168.1.1

//autostart binarie

sudo crontab -e @reboot sleep 10 && cd /home/pi/openFrameworks/apps/myApps/<yourAppFile>/bin && ./<yourAppName>

//do not set network to sleep

sudo iw wlan0 set power_save off

//https://www.bitpi.co/2015/02/14/prevent-raspberry-pi-from-sleeping/

sudo nano /etc/xdg/lxsession/LXDE-pi/autostart
