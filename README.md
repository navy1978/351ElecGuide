<h1>Guide to install a VM with Ubuntu 20.10 and compile 351Elec.</h1>

1) Download Ubuntu 20.10 from here: https://ubuntu.com/download/desktop
2) Download Oracle VM from here: https://www.virtualbox.org/
3) Create a VM followign these steps:https://brb.nci.nih.gov/seqtools/installUbuntu.html (IMPORTANT: give the VM more than 45 GB I gave it 120GB)
4) Once the process is finished executre the following commands:
<ol>
    <li>sudo apt update && sudo apt upgrade</li>
    <il>sudo apt install gcc make git unzip wget xz-utils libsdl2-dev libsdl2-mixer-dev libfreeimage-dev libfreetype6-dev libcurl4-openssl-dev rapidjson-dev libasound2-dev libgl1- mesa-dev build-essential libboost-all-dev cmake fonts-droid-fallback libvlc-dev libvlccore-dev vlc-bin texinfo premake4 golang libssl-dev curl patchelf xmlstarlet patchutils gawk gperf xfonts-utils default-jre python xsltproc libjson-perl lzop libncurses5-dev device-tree-compiler u-boot-tools rsync g++-9 libnss3-dev libtiff5-dev libxml-parser-perl libparse-yapp-perl unrar</li>
</ol>
After that you can restart your machine

5) In order to have also the copy-paste between your OS and the VM execute the following
    sudo apt-get install virtualbox-guest-additions-isosudo 
    mount -o loop /usr/share/virtualbox/VBoxGuestAdditions.iso /mnt
    cd /mnt
    /autorun.sh

6) clone and build using the following commands (with a user that is not root

    git clone https://github.com/fewtarius/351ELEC.git 351ELEC  
    cd 351ELEC  
    make clean
    make world
    
 (or make RG351P only for RG351P)
