Ansible role: timesync
======================

An Ansible role for managing systemd-timesyncd

Requirements
------------

None.

Role Variables
--------------
```
ntp_servers:
  - 0.pool.ntp.org
  - 1.pool.ntp.org
  - 2.pool.ntp.org
  - 3.pool.ntp.org
```

Dependencies
------------

None.

Example Playbook
----------------


    - hosts: all
      roles:
         - { role: sgaduuw.timesyncd, ntp_servers: [ '0.pool.ntp.org', '1.pool.ntp.org', '2.pool.ntp.org', '3.pool.ntp.org' ] }

License
-------

MIT

Author Information
------------------

Created by Sgaduuw, 2020
