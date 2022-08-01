Ansible Role: Grub2 Boot Loader Settings
=========

Ansible role to configure Grub2 boot loader security settings on Linux Servers.

Requirements
------------

The role does not require anything to run on RHEL and its derivatives.

Dependencies
------------

None.

Example Playbook
----------------

``` yaml
    - hosts: servers
      roles:
         - role: mikepruett3.grub-security
```

License
-------

MIT

Author Information
------------------

Role created by [mikepruett3](https://github.com/mikepruett3) on [Github.com](https://github.com/mikepruett3/ansible-role-grub-security)
