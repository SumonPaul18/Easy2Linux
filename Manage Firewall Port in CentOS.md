# Manage Firewall Port in CentOS
Ref: https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-using-firewalld-on-centos-7
#
Check Port Status
####
    netstat -na | grep 55555

Check Port Status in iptables

    iptables-save | grep 55555

Add the port

    nano /etc/services
    Example: service-name  port/protocol  [aliases ...]   [# comment]
    testport        55555/tcp   # Application Name

Open firewall ports

    firewall-cmd --zone=public --add-port=55555/tcp --permanent

Reload Firewall services

    firewall-cmd --reload
