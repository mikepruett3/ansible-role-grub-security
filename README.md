Ansible Role: Grub2 Boot Loader Settings
=========

Ansible role to configure Grub2 boot loader security settings on Linux Servers.

Requirements
------------

The role does not require anything to run on RHEL and its derivatives.

Role Variables
--------------

Available variables are listed below, along with default values (see ```defaults/main.yml```):

``` yaml
grub_pass: "grub.pbkdf2.sha512.00000.XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX.XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
grub_timeout: "10"
enable_apparmor: True
```

```grub_pass``` **(Required)** The encrypted password to assign to the Grub Bootloader. Made using grub-mkpasswd-pbkdf2.

```grub_timeout``` **(Required)** The ammount (in seconds) to display the Grub Boot Menu on startup.

```enable_apparmor``` **(Required)** If AppArmor is installed, this switch (True or False) will configure AppArmor to start at boot.

Role variables can be stored with the ```hosts.yaml``` file, or in the main variables file.

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
