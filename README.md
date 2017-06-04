Shaarli for nginx
=================

[![Build Status](https://travis-ci.org/MicroJoe/ansible-role-shaarli.svg?branch=master)](https://travis-ci.org/MicroJoe/ansible-role-shaarli)

A Shaarli role for nginx.

Requirements
------------

To be defined.

A Debian Jessie box with nginx should be fine.

Role Variables
--------------

- `shaarli_source` URL to retrieve the Shaarli archive from. Defaults to Github
  archive for v0.9.0 release
- `shaarli_base` Base directory to put Shaarli installation into. Defaults to
  `/var/www/shaarli`
- `shaarli_user` Owner of the files. Defaults to dedicated `shaarli` user.
- `shaarli_group` Group of the files. Defaults to required `www-data` group for
  php-fpm access.
 - `shaarli_servername` Name of the vhost. Defaults to `shaarli.localhost`.

Dependencies
------------

To be defined.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: MicroJoe.shaarli, shaarli_servername: shaarli.example.com }

License
-------

MIT.

Author Information
------------------

Romain Porte.
