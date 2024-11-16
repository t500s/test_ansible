power
=========

Role for disabling c-state and disable power-saving mode

- Disabling C-state for all available CPUs.
- Switching CPU operation from power-saving mode to more productive mode.

Example Playbook
----------------
```
    - hosts: servers
      roles:
         - role: power
```
