<h1>351Elec develpment environmet (install a VM with Ubuntu 20.10 and compile 351Elec.)</h1>
<ol>
   <li>Download Ubuntu 20.10 from here: https://ubuntu.com/download/desktop</li>
   <li>Download Oracle VM from here: https://www.virtualbox.org/</li>
   <li>Create a VM followign these steps:https://brb.nci.nih.gov/seqtools/installUbuntu.html (IMPORTANT: give the VM more than 45 GB I gave it 120GB)</li>
   <li>Once the process is finished executre the following commands:</li>
   <ul>
      <li>sudo apt update && sudo apt upgrade</li>
      <li>sudo apt install gcc make git unzip wget xz-utils libsdl2-dev libsdl2-mixer-dev libfreeimage-dev libfreetype6-dev libcurl4-openssl-dev rapidjson-dev libasound2-dev libgl1- mesa-dev build-essential libboost-all-dev cmake fonts-droid-fallback libvlc-dev libvlccore-dev vlc-bin texinfo premake4 golang libssl-dev curl patchelf xmlstarlet patchutils gawk gperf xfonts-utils default-jre python xsltproc libjson-perl lzop libncurses5-dev device-tree-compiler u-boot-tools rsync g++-9 libnss3-dev libtiff5-dev libxml-parser-perl libparse-yapp-perl unrar</li>
   </ul>
   After that you can restart your machine
   <li> In order to have duest addition and also enable copy&paste between VirtualBox Host and Guest Machines execute the following</li>
   <ul>
      <li> sudo apt-get install virtualbox-guest-additions-isosudo</li>
      <li>mount -o loop /usr/share/virtualbox/VBoxGuestAdditions.iso /mnt</li>
      <li>cd /mnt</li>
      <li>/autorun.sh</li>
   </ul>
   <li>For copy paste follow this:https://www.liberiangeek.net/2013/09/copy-paste-virtualbox-host-guest-machines/</li>
   <li>Clone and build using the following commands (with a user that is not root)</li>
   <ul>
      <li>git clone https://github.com/fewtarius/351ELEC.git 351ELEC</li>
      <li>cd 351ELEC</li>
      <li>make clean</li>
      <li>make world</li>
   </ul>
   (or make RG351P only for RG351P)
</ol>
