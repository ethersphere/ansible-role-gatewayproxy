# Ansible Role: bee

This repository contains sample code for automating bee installation and management using Ansible.

[Ansible](https://www.ansible.com/) is a radically simple IT automation engine that automates cloud provisioning, configuration management, application deployment, intra-service orchestration, and many other IT needs.
[gateway-proxy](https://github.com/ethersphere/gateway-proxy/) it's proxy service for the Bee client.

## Installation

### Ansible Galaxy
Use `ansible-galaxy install ethersphere.gateway-proxy` to install the latest stable release of the role on your system. Alternatively, if you have already installed the role, use `ansible-galaxy install -f ethersphere.gateway-proxy` to update the role to the latest release.

### Git
Use git clone https://github.com/ethersphere/ansible-role-gateway-proxy.git to pull the latest edge commit of the role from GitHub.

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
    - role: ethersphere.gateway-proxy
  vars:
    bee_config:
      swap-endpoint: https://rpc.gnosischain.com/
      swap-initial-deposit: 0
```

`host_vars/x.x.x.x.yml`
```
swarm_key: '{"address":"b7bacdcafac7adb97df33b2c76922425a0bf0fc1","crypto":{"cipher":"aes-128-ctr","ciphertext":"739ea31cad0a116823d12155cf1f3da987200f70322ea6ef3b4f13cca38346c1","cipherparams":{"iv":"9eaac7d8ff2dc63d683900afcde1ede0"},"kdf":"scrypt","kdfparams":{"n":32768,"r":8,"p":1,"dklen":32,"salt":"a89f5e12b820ee917dca59a83a1359fd0b7d892bcec1c0aa37c102ee73749a4c"},"mac":"e1b124a8f3d08d382af3331e56c1666227429680bfca9461c2de79f98d731807"},"version":3,"id":"d834a5ad-6a36-4a27-8116-53370df83ffa"}'
password: my-password
```
