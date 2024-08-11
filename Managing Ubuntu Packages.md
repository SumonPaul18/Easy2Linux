# Managing Ubuntu Packages

Find installed packages
####
    apt list --installed
####
Find specefic package

    apt list -a bind9
####
Find specefic package using grep

    apt list | grep postfix
####
    dpkg --list | grep postfix
#
Remove Packages from ubuntu
####
    apt-get --purge remove openssh-server
