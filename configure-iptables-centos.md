# How to configure iptables on CentOS
Install iptables-services
####
    yum install iptables-services -y
Manage iptables-services
####
    systemctl status iptables
    systemctl start iptables
    systemctl enable iptables
####
Disable iptables Services

    systemctl disable iptables
    
List of Listing current rules
####
    iptables -L
####
Listing iptables roles with line numbers

    iptables -L --line-numbers

Adding new iptables rules <br>
iptables -A INPUT -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT
####
Adding ssh in iptables roles

    iptables -A INPUT -p tcp --dport ssh -j ACCEPT
####
Adding 80 port in iptables roles

    iptables -A INPUT -p tcp --dport 80 -j ACCEPT

Saving and restoring rules
####
    service iptables save
