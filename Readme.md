


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



conjure-down --- (remove)

sudo snap remove conjure-up (remove)
