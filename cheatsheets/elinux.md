#Enterprise Linux

## Network

| Command							| Meaning
| :---                  			| :---
| `ip address, ip a`				| Ip addresses
| `ip route, ip r	`				| Route table
| `cat /etc/resolv.conf`			| DNS


## Systemctl

| Command							| Meaning
| :---                  			| :---
| `systemctl list-units --type service`				| List of services
| `sudo systemctl status httpd.service`				| check status of service (httpd)
| `sudo systemctl start httpd.service`				| Start service (httpd)
| `sudo systemctl stop httpd.service`				| Stop service (httpd)
| `sudo systemctl list-unit-files`					| List of services (+ static, disabled)
| `sudo systemctl kill httpd.service`				| Kill service (httpd) (add -s SIGKILL to force)
| `sudo systemctl enable/disable httpd.service`	| Start/stop httpd on boot

## Firewalld

| Command							| Meaning
| :---                  			| :---
| `firewall-cmd --state`			| State of firewall
| `firewall-cmd [--permanent] [--zone=ZONE] --add-service=http`				| Enable a service in zone

Configuration is stored in /etc/firewalld and /usr/lib/firewalld

TODO

yum update provides (en overlopen/committen checklist lamp, dns)

## Resources
[Github Bertvv](https://github.com/bertvv/cheat-sheets/blob/master/src/EL7.md "Bertvv")

