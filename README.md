# Ansible Role: PHP PECL extensions

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Installs PHP PECL extensions (and optionally `pecl` itself) on servers with PHP already installed.

## Requirements

PHP must already be installed on the server. This role works great with and is tested alongside `geerlingguy.php`.

Also, if you don't already have `php-pear` (RedHat) or `php-pecl` (Debian) installed, you should set `php_pecl_install_pecl: true` to force this role to install the proper package.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_pecl_install_pecl: false

Whether to install `php-pecl` (Debian-based OSes) or `php-pear` (RedHat-based OSes).

    php_pecl_install_command: "pecl install"

The command that will be run to install extensions. You should override this default with `"pecl install -Z"`

    php_pecl_extensions: []

A list of extensions that should be installed via `pecl install`. If you'd like to have this role install extensions like XDebug, just add it in the list, like so:

    php_pecl_extensions:
      - redis
      - xdebug

## Dependencies

  - nholuong.php

## Example Playbook

    - hosts: webservers
      vars_files:
        - vars/main.yml
      roles:
        - nholuong.php-pecl

*Inside `vars/main.yml`*:

    php_pecl_extensions:
      - redis
      - xdebug

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟