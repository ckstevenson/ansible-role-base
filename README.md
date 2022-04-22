Role Name
=========

My base playbook for my homelab and other systems.

Requirements
------------

Everyting to use this role is satisfied with the ansible.builtin collection.

Role Variables
--------------

./defaults/main.yml
```.yml
hostname: 'hostname'
user: 'user'
```

Dependencies
------------

No role dependencies.

Dev Dependencies
------------

* python-poetry
* [just](https://github.com/casey/just)
* Virtualbox (need to switch with KVM/QEMU)
* Vagrant

Example Playbook
----------------

```.yml
---
# example playbook to configure base imahe

- name: Headscale
  hosts: all
  become: true
  vars:
    user: 'cameron'
    hostname: 'homelab'
  tasks:
    - name: "Include ckstevenson.base"
      include_role:
        name: "ckstevenson.base"
```

License
-------

MIT
