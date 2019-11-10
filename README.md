Basic
-----

* sudo apt-get install network-manager-openvpn

* sudo apt-get install curl

Kernel
------

* sudo apt-get install ukuu

GIT
---

* sudo apt-get install git

* git config --global user.name "testuser"

* git config --global user.email "testuser@example.com"

* ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

* eval "$(ssh-agent -s)"

* ssh-add ~/.ssh/id_rsa

* sudo apt-get install xclip

* xclip -sel clip < ~/.ssh/id_rsa.pub

* Config transfer to usb speed 

*in sudo su

* echo $((16*1024*1024)) > /proc/sys/vm/dirty_background_bytes

* echo $((48*1024*1024)) > /proc/sys/vm/dirty_bytes

Docker 
-------

* sudo apt install docker.io

* sudo systemctl start docker

* sudo systemctl enable docker

* sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose

* sudo chmod +x /usr/bin/docker-compose

* sudo groupadd docker

* sudo usermod -aG docker $USER

For docker xdebug
-----------------

* sudo ufw allow in on docker0 from 172.17.0.0/24 to 172.17.0.1/32 port 9000 comment xdebug
* sudo iptables -I INPUT -p tcp -m tcp --dport 9000 -j ACCEPT
 
* sudo iptables -A INPUT -p tcp --dport 9000 -j ACCEPT
