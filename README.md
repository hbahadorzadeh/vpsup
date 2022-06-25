# vpsup
A project to setup all services you need on your VPS using docker-compose

Remember to stop systemd-resolve --> $ sudo systemctl stop systemd-resolved.service

Edit /etc/resolv.conf & add nameserver for Ex. nameserver 8.8.8.8 to avoid conectivity issues (DNS) 

$ cd vpsup

To set mydomain.com , Cloudflare Api token for traefik & ...

$ nano .env

Do Not forget to add ss-config.js for shadowsocks

It is recommended to use docker-compose version 1.25.0 , otherwise shadowsocks may fail

$ sudo curl -SL https://github.com/docker/compose/releases/download/1.25.0/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose && sudo /usr/local/bin/./docker-compose up -d
