Ansible Role: Nginx
===================

This role do a simple install of latest Nginx Web Werver from official repo, on Centos/Rhel 6/7 and Ubuntu.


Requirements
------------

This Ansible playbook is meant to be run on a FRESH never used server, virtual machine or container.

Role Variables
--------------

**vars/:***
```
Debian.yml
RedHat.yml
```

Role Templates
==============

None.

Dependencies
------------

None.

Example Playbook
----------------

**Example with prompt:**
```
- hosts: "{{ vm }}"
  gather_facts: True

  vars_prompt:
    - name: "vm"
      prompt: "VM"
      private: no

  roles:
    - { role: squintans.nginx }
```

Playbook Call
=============
```
ansible-playbook -i inventory.yml play.yml
```

License
-------

GPLv2

Author Information
------------------
This role was created in 2019 by Serafín Quintáns - [squintans](http://www.linkedin.com/in/serafin-quintans/)