Ansible role: timesyncd
=======================

An Ansible role for managing systemd-timesyncd, the systemd built-in NTP client.

Requirements
------------

None.

Role Variables and their defaults
--------------
The variables used in this role with their defaults as example:
```
ntp_timezone: Etc/UTC
ntp_servers:
  - 0.pool.ntp.org
  - 1.pool.ntp.org
  - 2.pool.ntp.org
  - 3.pool.ntp.org
ntp_servers_fallback: []
```
The default for `ntp_servers_fallback` is an empty list. To make use of fallback NTP servers, simply create a list of servers, eg:
```
ntp_servers_fallback:
  - time1.google.com
  - time2.google.com
  - time3.google.com
  - time4.google.com
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

Created by Eelco Wesemann (Sgaduuw), 2020
