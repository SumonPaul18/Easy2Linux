# Configure Nginx Port in Linux
How to Configure Nginx Port in Linux

Find nginx source files location.

    whereis nginx

Open NGINX configuration file

On Debian/Ubuntu

    vi /etc/nginx/sites-enabled/default  
On CentOS/RHEL

    vi /etc/nginx/nginx.conf             

Change NGINX port number

Look for the line that begins with listen inside server block. It will look something like
####
    server {
            listen 80 default_server;
            listen [::]:80 default_server;
            ...
            Change port number 80 to 8080 in above lines, to look like

    server {
            listen 8080 default_server;
            listen [::]:8080 default_server;

Check syntax of your updated config file.

    nginx -t

Restart Nginx Services

On Debian/Ubuntu

    service nginx reload        
 On CentOS/RHEL
 
    systemctl restart nginx    

Verify local network sockets table

    netstat -tlpn| grep nginx

    ss -tlpn| grep nginx

End Change Nginx Port
