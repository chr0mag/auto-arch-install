# auto-arch-install
Bash script to automate the base Arch Linux installation.

###### Intended Use
This script is intended for use by experienced Arch users already familiar with the official [Arch Linux instllation](https://wiki.archlinux.org/index.php/Installation_guide) process. This is meant to be used as a quick & simple way to spin up testing environments, often virtual images, or any other instance where a fresh base Arch Linux installation is desired.

###### Non-intended Use
This script is not meant for new Arch users looking for a way to skip the manual installation. If you've ended up here because you're searching for short cuts, then Arch Linux is probably not the distribution for you.

###### Assumptions
This script makes a whole host of assumptions about the system on which it is run.  Below are a few of the more glaring assumptions any script user should be aware of.
* single virtual disk (eg. /dev/vda)
* UEFI boot enabled
* running on a network w/DHCP enabled
* execution from a system booted using the latest [Arch Linux Install Image](https://www.archlinux.org/download/)

###### Resulting System
* GPT partition scheme with 550MiB Efi System Partition (ESP) (mountpoint /boot) and remainder for root (mountpoint /)
* no SWAP partition; (a [swapfile](https://wiki.archlinux.org/index.php/Swap#Swap_file) can easilly be added post-install)
* simple iptables stateful [firewall](https://wiki.archlinux.org/index.php/Simple_stateful_firewall) enabled with SSH port 22 open
* SSHd enabled with only the provided $USER allowed

###### Sources
* https://shirotech.com/linux/how-to-automate-arch-linux-installation - similar project
* https://wiki.archlinux.org/ - the official Arch Linux wiki
