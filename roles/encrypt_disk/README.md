encrypt_disk
=========

Role for encryption partition and block device

- Implement the procedure of encrypting the second disk in the system (where there is no root partition) (partition name should be specified in the inventory)
- Implement a procedure to encrypt the partition that is present on the disk next to the root partition.

Role Variables
--------------

enc_block_device - the second disk in the system 
enc_device: enc1 - name for opened luks container
enc_password - password for luks container
enc_luks_version - luks version

enc_secondary_partition - next partitions for encrypting. Can be set manual. If False next to the root partition
enc_secondary_device:  name for opened luks container
enc_secondary_password: password for luks container
enc_secondary_luks_version: luks version
open_luks - open luks?

All defaults in `default/main.yml`

Example Playbook
----------------
```
    - hosts: servers
      roles:
         - role: encrypt_disk
```
