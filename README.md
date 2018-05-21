# Ansible role: dnsmasq
DHCP and local caching DNS server.
I use this to serve my VPN.

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ 

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
