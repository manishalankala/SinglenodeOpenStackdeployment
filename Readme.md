


sudo snap install lxd

sudo lxd init

sudo usermod -a -G lxd <username>
  
newgrp lxd

sudo snap install conjure-up --classic

or 

sudo snap install conjure-up --classic --beta

or 

sudo snap refresh conjure-up --classic --edge


/snap/bin/lxc storage list

/snap/bin/lxc storage show default

/snap/bin/lxc network create lxdbr0 ipv4.address=auto ipv4.nat=true ipv6.address=none ipv6.nat=false (optional)

/snap/bin/lxc network show lxdbr0

/snap/bin/lxc profile show default

lxc profile show default 

conjure-up



# reference screenshot

![image](https://user-images.githubusercontent.com/33985509/77768071-43733e80-7042-11ea-8541-c1497aced8fe.png)


which juju

/snap/bin/juju

manish_chintu91@instance-1:~$ juju version

2.6.10-bionic-amd64

manish_chintu91@instance-1:~$ which conjure-up

/snap/bin/conjure-up

manish_chintu91@instance-1:~$ conjure-up --version

conjure-up 2.6.10

manish_chintu91@instance-1:~$ which lxc

/snap/bin/lxc

manish_chintu91@instance-1:~$ cat /etc/lsb-release

DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=18.04
DISTRIB_CODENAME=bionic
DISTRIB_DESCRIPTION="Ubuntu 18.04.4 LTS"

manish_chintu91@instance-1:~$ lxc version
Client version: 3.23
Server version: 3.23


# Errors

cat /home/manish_chintu91/.cache/conjure-up/conjure-up.log

![image](https://user-images.githubusercontent.com/33985509/77767622-a3b5b080-7041-11ea-96f2-66231353454e.png)

![image](https://user-images.githubusercontent.com/33985509/77767548-87197880-7041-11ea-9651-8ef7699e37de.png)



# refrences

https://github.com/conjure-up/conjure-up/issues/1590

https://github.com/conjure-up/conjure-up/issues/1308


```
sudo apt-get update; sudo apt-get upgrade -y; sudo snap install lxd; sudo snap install conjure-up --classic; /snap/bin/lxd init --auto; /snap/bin/lxc network create lxbr0 ipv4.address=auto ipv4.nat=true ipv6.address=none ipv6.nat=false

conjure-up or conjure-up openstack

```

# Uninstall


conjure-down --- (remove)

sudo snap remove conjure-up (remove)


