zookeeper
=========
This is the zookeeper role for ansible.

Dependencies
------------
- java

Usage
-----

```
#requirements.yml
---
- src: git+ssh://git@github.com:samskd/ansible_role_zookeeper.git
  name: zookeeper

#/bin/bash
> ansible-galaxy install -r requirements.yml

#playbook.yml
---
- hosts: all
  become: true
  become_method: sudo
  roles:
    - zookeeper

#/bin/bash
> ansible-playbook -i inventory playbook.yml --tags "deploy,restart"

Available tags:
deploy - Install and configures zookeeper
restart - Restarts zookeeper service
configure - Configures zookeeper
stop - Stops zookeeper service
```
