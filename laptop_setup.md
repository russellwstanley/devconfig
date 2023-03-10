Hi Russel, after install please add this to grub: i8042.nomux=1

So it will look like this: GRUB_CMDLINE_LINUX_DEFAULT="quiet splash i8042.nomux=1"

Also please run this command to install the control center for fan control and keyboard backlight: sudo echo 'deb http://deb.tuxedocomputers.com/ubuntu focal main' > /etc/apt/sources.list.d/controlcenter.list && wget -O - http://deb.tuxedocomputers.com/0x54840598.pub.asc | sudo apt-key add - && sudo apt-key adv --fingerprint 54840598 && sudo apt update && sudo apt install tuxedo-control-center linux-headers-$(uname -r) -y
