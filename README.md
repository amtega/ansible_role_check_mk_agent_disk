# Ansible check_mk_agent_steal_time role

This is an [Ansible](http://www.ansible.com) role setup Check_MK plugin to check disks.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - role: amtega.check_mk_agent_disks
      vars:
        check_mk_agent_disk_list:
          - name: onemount
            path: /mnt/onemount
            warning: 10%
            critical: 5%
          - name: othermount
            path: /mnt/othermount
            warning: 10%
            critical: 5%
```

## Testing

Tests are based on [molecule with docker containers](https://molecule.readthedocs.io/en/latest/installation.html).

```shell
cd amtega.check_mk_agent_disks

molecule test --all
```

## License

Copyright (C) 2022 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García
