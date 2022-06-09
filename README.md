# Ansible Role: bee

This repository contains sample code for automating bee installation and management using Ansible.

[Ansible](https://www.ansible.com/) is a radically simple IT automation engine that automates cloud provisioning, configuration management, application deployment, intra-service orchestration, and many other IT needs.
[gateway-proxy](https://github.com/ethersphere/gateway-proxy/) it's proxy service for the Bee client.

## Installation

### Ansible Galaxy
Use `ansible-galaxy install ethersphere.gatewayproxy` to install the latest stable release of the role on your system. Alternatively, if you have already installed the role, use `ansible-galaxy install -f ethersphere.gatewayproxy` to update the role to the latest release.

### Git
Use git clone https://github.com/ethersphere/ansible-role-gatewayproxy.git to pull the latest edge commit of the role from GitHub.

## Example

Deploy one gateway-proxy node on a defined host

`hosts`
```
[my-hosts]
x.x.x.x
```

`playbook.yml`
```
---
- hosts: my-hosts

  roles:
    - role: ethersphere.gatewayproxy
  vars:
    gatewayproxy_config:
      port: 8080
```
