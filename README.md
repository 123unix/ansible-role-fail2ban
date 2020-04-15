fail2ban
=========

Install **fail2ban** and configure it with more practical settings.

Specifically,
  * make fail2ban ban whole subnets
      *  /16 by default, but configurable, instead of the stock ban by hosts (/32)
  * **DROP** packets from the banned hosts instead of REJECT
  * increase **bantime** and **findtime** timers
  * make DB records more persistent (25 days instead of the default 1 day)

The role includes customizations for a number of builtin jails. Currently Asterisk and FreeSWITCH jails received customizations.

Requirements
------------

Any system covered by Ansible itself and having fail2ban in its main package system should be supported.

Role Variables
--------------

All settable variables are listed in defaults/main.yml with comments on their usage.

Example Playbook
----------------

    - hosts: servers
      roles:
      - 123unix.fail2ban

License
-------

GPL v.3

Author Information
------------------

Created by [Alexander Shcheblikin](https://www.123unix.com)
