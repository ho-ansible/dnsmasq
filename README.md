# Ansible role: dnsmasq
DHCP and local caching DNS server.
I use this to serve my VPN.

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `dnsmasq_interface` (default: lo): network interface to bind to
+ `dnsmasq_domains`: "domain" lines (see dnsmasq.conf (5))
+ `dnsmasq_hosts`: static host entries
+ `dnsmasq_servers`: upstream servers 
+ `dnsmasq_dhcp_ranges`: DHCP server config
+ `dnsmasq_dhcp_hosts`: static IPs issued via DHCP
+ `dnsmasq_dhcp_opts`: options issued with DHCP lease
+ `dnsmasq_cnames`: (target, source) pairs
+ `adblock_urls`: (name, URL) pairs
+ `dnsmasq_user` (default: dnsmasq): unprivileged user to run as
+ `dnsmasq_group` (default: dip): unprivileged group to run as
+ `dnsmasq_conf_dir` (default: '/etc/dnsmasq.d/'): where all config
  is stored (must end in slash)
+ `dnsmasq_log` (default: /var/log/dnsmasq): logfile

## Dependencies
None.

## Example Playbook

```
- hosts: dns
  roles:
    - { role: ho-ansible.dnsmasq }
```

## License
MIT

## Author Information
Sean Ho, https://github.com/ho-ansible/
