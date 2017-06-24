Shaarli for nginx
=================

[![Build Status](https://travis-ci.org/MicroJoe/ansible-role-shaarli.svg?branch=master)](https://travis-ci.org/MicroJoe/ansible-role-shaarli)

A Shaarli role for nginx.

Requirements
------------

To be defined.

- Debian Stretch (wont work with Jessie)
- Nginx
- Letsencrypt

Role Variables
--------------

- `shaarli_version` Shaarli version. Default: 0.9.0
- `shaarli_source` URL to retrieve the Shaarli archive from. Default: Github
  archive
- `shaarli_base` Base directory to put Shaarli installation into. Default:
  `/var/www/shaarli`
- `shaarli_user` Owner of the application files. Default: dedicated `shaarli`
  user
- `shaarli_group` Group assigned to the application files. Default: required
  `www-data` group for php-fpm access

### Nginx configuration file

- `shaarli_nginx_server_name` Server name for the nginx configuration file.
  Default: `shaarli.localhost` so that users can register root account before
  setting up public access
- `shaarli_nginx_filename` Name of the configuration file that will be placed
  in `/etc/nginx/sites-available`. Default: `shaarli.conf`

### Letsencrypt support

- `letsencrypt_wellknown` Directory path of the LetsEncrypt directory used for
  certificate validation. Default: `/var/www/letsencrypt`
- `letsencrypt_activate` Activate LetsEncrypt and HTTPS support. Default: false
- `letsencrypt_https` Activate HTTPS server and redirect HTTP to HTTPS. This is
  to be activated only when you have your certificate ready. If you want to
  verify yourself using LetsEncrypt webroot checker only enable
  `letsencrypt_activate` but keep this option to false first.

Dependencies
------------

To be defined.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: shaarli
          shaarli_nginx_server_name: myshaarly.example.com
          tags: [shaarli]
          letsencrypt_activate: true
          letsencrypt_https: true # disable for verify first

License
-------

MIT.

Author Information
------------------

Romain Porte.
