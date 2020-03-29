


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


# Ticket

https://github.com/conjure-up/conjure-up/issues/1647





-----------------------------------------------------------------------------------------------------------------------------------------------------


Single Node ("All in One") Deployments

# Cloud Controller

A minimum of 2 GB of RAM is recommended

64-bit x86 processor - Intel 64 or AMD64 

AMD-V or Intel VT hardware virtualization extensions enabled.

A minimum of 50 GB of available disk space is recommended

Network Interface Cards -  1 x 1 Gbps Network Interface Card


# Compute Nodes

64-bit x86 processor with support for the Intel 64 or AMD64 CPU extensions, and the AMD-V or Intel VT hardware virtualization extensions enabled.

A minimum of 2 GB of RAM is recommended.

minimum of 50 GB of available disk space

Network Interface Cards - 2 x 1 Gbps Network Interface Cards



sudo apt update

sudo apt install openjdk-8-jdk

java -version

openjdk version "11.0.6" 2020-01-14

OpenJDK Runtime Environment (build 11.0.6+10-post-Ubuntu-1ubuntu118.04.1)

OpenJDK 64-Bit Server VM (build 11.0.6+10-post-Ubuntu-1ubuntu118.04.1, mixed mode)

sudo apt-get install python3

sudo apt-get upgrade python3

grep --color vmx /proc/cpuinfo

grep --color svm /proc/cpuinfo


sudo apt install qemu qemu-kvm libvirt-bin  bridge-utils  virt-manager -y


![image](https://user-images.githubusercontent.com/33985509/77857587-ae697480-71fe-11ea-9821-a556b8d15fd8.png)

sudo apt update

sudo apt -y upgrade

sudo useradd -s /bin/bash -d /opt/stack -m stack

echo "stack ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/stack

sudo su - stack

git clone https://opendev.org/openstack/devstack

cd devstack

cd samples

sudo cp local.conf /opt/stack/devstack

changes as below local.conf

```
[[local|localrc]]
FLOATING_RANGE=192.168.1.224/27
FIXED_RANGE=10.128.0.15/24
ADMIN_PASSWORD=password
DATABASE_PASSWORD=password
RABBIT_PASSWORD=password
SERVICE_PASSWORD=password

```

![image](https://user-images.githubusercontent.com/33985509/77860299-c34e0400-720e-11ea-87cb-0b2e9e6c2e94.png)

http://10.128.0.15/dashboard

http://10.128.0.15/identity/

http://34.71.186.50/dashboard/project/

admin

password


