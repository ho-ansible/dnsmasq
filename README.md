# Ansible role: dnsmasq
DHCP and local caching DNS server.
I use this to serve my VPN.

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `dnsmasq_interface` (default: lo): network interface to bind to
+ `dnsmasq_port` (default: 53): UDP port to listen on (and open firewall)
+ `dnsmasq_hosts`: list of (IP, host) tuples of static host entries
+ `dnsmasq_servers`: list of IPs of upstream DNS servers 
+ `dnsmasq_dhcp_hosts`: list of static IPs issued via DHCP
+ `dnsmasq_dhcp_opts`: list of options issued with DHCP lease
+ `dnsmasq_host_urls`: dict of (name, URL) pairs for additional static hosts
+ `dnsmasq_includes`: dict of (name, URL) config file pairs for `conf-dir`
+ `dnsmasq_config`: multiline text to be inserted directly into `/etc/dnsmasq.conf`
+ `dnsmasq_user` (default: dnsmasq): unprivileged user to run as
+ `dnsmasq_group` (default: dip): unprivileged group to run as
+ `dnsmasq_conf_dir` (default: '/etc/dnsmasq.d'): where all config is stored 

## Playbooks
+ `main.yml`: apply dnsmasq role
+ `uninstall.yml`: remove dnsmasq. Run before removing config from inventory.

## Dependencies
+ [ho-ansible.systemd-networkd](https://github.com/ho-ansible/systemd-networkd)

## License
+ Ansible role licensed [MIT](LICENSE)

## Author Information
+ Ansible role by [Sean Ho](https://github.com/ho-ansible/)
