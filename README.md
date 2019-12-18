# Ansible role: dnsmasq
DHCP and local caching DNS server.
I use this to serve my VPN.

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `dnsmasq_interface` (default: lo): network interface to bind to
+ `dnsmasq_hosts`: static host entries
+ `dnsmasq_servers`: upstream DNS servers 
+ `dnsmasq_dhcp_hosts`: static IPs issued via DHCP
+ `dnsmasq_dhcp_opts`: options issued with DHCP lease
+ `dnsmasq_host_urls`: dict of (name, URL) pairs
+ `dnsmasq_config`: multiline text to be inserted directly into `/etc/dnsmasq.conf`
+ `dnsmasq_user` (default: dnsmasq): unprivileged user to run as
+ `dnsmasq_group` (default: dip): unprivileged group to run as
+ `dnsmasq_conf_dir` (default: '/etc/dnsmasq.d'): where all config is stored 

## Dependencies
None.

## License
Ansible role licensed [MIT](LICENSE).

## Author Information
Sean Ho, https://github.com/ho-ansible/
