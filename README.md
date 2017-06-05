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

- `shaarli_source` URL to retrieve the Shaarli archive from. Default Github
  archive for v0.9.0 release
- `shaarli_base` Base directory to put Shaarli installation into. Default
  `/var/www/shaarli`
- `shaarli_user` Owner of the application files. Default dedicated `shaarli`
  user
- `shaarli_group` Group assigned to the application files. Default required
  `www-data` group for php-fpm access

Ngnix-related variables:

- `shaarli_nginx_server_name` Name of the vhost. Default `shaarli.localhost`
- `shaarli_nginx_listen` Listed directive for nginx. Default `80`
- `shaarli_nginx_filename` Configuration file name for nginx. Default
  `shaarli.conf`

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
