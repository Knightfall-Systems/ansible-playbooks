Proxmox Purge
=========

This role is to purge an lxc container on a proxmox cluster based on given parameters.

Requirements
------------

The proxmoxer and requests python modules must be installed on the machine running this role. In the inventory, hosts representing the Proxmox cluster nodes must be defined. Additionally, all hosts representing containers to be purged must have {{ vmid }} defined. See defaults/main.yml and the ansible proxmox_module documentation for more information and examples. Ansible version 2.10+ required.

Role Variables
--------------

Aside from host variables mentioned in the requirements section, the api_host, api_user, and api_password variables must be passed to the role or predefined in the defaults/main.yml or vars/main.yml files.

Dependencies
------------

The only dependency is on the proxmoxer and requests python modules as well as the ansible proxmox_module from community.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: services
      gather_facts: no
      roles: 
      - proxmox-purge

License
-------

MIT

Author Information
------------------

Knightfall Systems LLC
Duncan Forsythe
https://github.com/Knightfall-Systems/ansible-playbooks
