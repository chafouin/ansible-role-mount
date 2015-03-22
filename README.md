Ansible Mount Role
==================

An ansible role for mounting devises.

Role Variables
--------------

```yaml
# list of dictionaries holding all devises that need to be mounted.
mount_devises:
  - name: /
    src: /dev/mapper/root
    fstype: ext4
    opts: noatime,errors=remount-ro
    state: mounted
    dump: 0
    passno: 1
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: MichaelRigart.mount }

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>