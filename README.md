# Ubuntu_add_vlans
Add vlan entries to to an interface

sudo apt-get install vlan

sudo nano /etc/network/interfaces.d/vlans

#add one entry below for each vlan where x=vlan#

auto eth0.x

iface eth0.x inet manual

  vlan-raw-device eth0

sudo systemctl restart networking.service
