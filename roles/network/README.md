network
=========

Role for rename default network dev. Only for netplan. 

-  Rename the active network interface to "net0". Display information about the renamed interface during the playbook

Role Variables
--------------

default_network_name - old network dev name
default_network_mac -  network dev mac
network_name - new name for network dev


All defaults in `default/main.yml`

Example Playbook
----------------
```
    - hosts: servers
      roles:
         - role: network
```
