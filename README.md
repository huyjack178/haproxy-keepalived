# ansible-haproxy-keepalived

A playbook building high availability Load Balancer with HAProxy and keepalived.

## Requirements

- [Ansible](http://docs.ansible.com/intro_installation.html)
- sshpass packet

## Overview

It will install high availability Load Balancer with HAProxy and keepalived.
You can customize it by edit vars file.
Tested on Ubuntu 14.04

## Usage

- Edit vars/main.yml
- Install to remote server.

Edit `ansible_hosts`.

```
default ansible_ssh_host=xxx.xxx.xxx.xxx ansible_ssh_port=22
```

Run playbook.

```bash
ansible-playbook site.yml -i ansible_hosts
```

## vars

```vars/main.yml
haproxy_bind_address: 10.19.10.111
haproxy_major_version: 1.8
```
