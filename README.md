## A simple Ansible playbook for use on OSX

**Can be tailored for your OS of choice if necessary by adjusting the "flash" role.**

This playbook will allow you to perform the following steps:

* Locally image an SD card on your computer with CentOS for ARM: 
[CentOS SIG AltArch Arm32](https://wiki.centos.org/SpecialInterestGroup/AltArch/Arm32)

* Copy required files to boot the Pi with defined values in _group_vars/all_

* Expand the filesystem to utilize the full SD capacity post boot-up

* Perform a _yum update_ and install any required packages defined in the variables (_rsyncd, httpd, cobbler, cobbler-web, etc_)

* Copy additional files specific to proper operation of cobbler and dependencies

* Create a new user account and add it to the _wheel_ group

* Download/Copy and install syslinux rpm for PXE boot

* Start and enable required services via systemctl

* Download/Copy and import CentOS x86_64 iso for imaging 
