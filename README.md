joenyland.nfs_server
=========================

[![CI](https://github.com/JoeNyland/ansible-nfs-server-role/actions/workflows/ci.yml/badge.svg)](https://github.com/JoeNyland/ansible-nfs-server-role/actions/workflows/ci.yml)

Installs NFS server and configures exports.

Requirements
------------

None.

Role Variables
--------------

### `nfs_exports`

A hash of exports to create

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: server
  roles:
    - role: joenyland.nfs_server
      vars:
        nfs_exports:
          /home:
            client_permissions:
              10.0.0.0/16:
                - rw # Allow read/write access
```

License
-------

MIT

Author Information
------------------

⌨️ with ❤️ by [Joe Nyland](https://joe.nyland.io)
