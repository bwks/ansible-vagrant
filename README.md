ansible-vagrant
=========

Ansible role to install the vagrant-libvirt provider

Requirements
------------

None 

Role Variables
--------------

```yaml
vagrant_version: "2.0.1"

vagrant_users:
  - "vagrant"

vagrant_plugins:
  - "vagrant-libvirt"

install_vagrant_libvirt: True

debian:
  download_url: "https://releases.hashicorp.com/vagrant/{{ vagrant_version }}/vagrant_{{ vagrant_version }}_x86_64.deb"
rhel:
  download_url: "https://releases.hashicorp.com/vagrant/{{ vagrant_version }}/vagrant_{{ vagrant_version }}_x86_64.rpm"

libvirt_network: 
  subnet: "192.168.121.1"
  mask: "255.255.255.0"
  dhcp_start: "192.168.121.10"
  dhcp_end: "192.168.121.254"
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
---
- hosts: all
  become: True

  roles:
    - role: ansible-vagrant
```

License
-------

GPLv3

Author Information
------------------

BoBtheButhcer
