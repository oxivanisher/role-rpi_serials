rpi_serials
===========
[![Ansible Lint](https://github.com/oxivanisher/role-rpi_serials/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-rpi_serials/actions/workflows/ansible-lint.yml)

Configure serial numbers for MPG2 and WVC1.

As always: Use at your own risk!

Role Variables
--------------

| Name                     | Comment                                   | Default value |
|--------------------------|-------------------------------------------|---------------|
| rpi_serials_mpg2         | The MPG2 serial number | ``       |
| rpi_serials_wvc1         | The WVC1 serial number | ``       |
| rpi_serials_rpi_boot_dev | The boot device where the `config.txt` is located. Will be overwritten if `raspberry_pi_boot_dev` is set! | `/dev/mmcblk0p1` |


Example Playbook
----------------

```yaml
- name: Configure multimedia serials
  hosts: rpis
  collections:
    - oxivanisher.raspberry_pi
  roles:
    - role: oxivanisher.raspberry_pi.rpi_serials
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.raspberry_pi](https://galaxy.ansible.com/ui/repo/published/oxivanisher/raspberry_pi/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-raspberry_pi).
