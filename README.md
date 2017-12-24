Boss Box
========

A modern, easy to configure, WordPress ready Vagrant box, perfect for local development.

Credits
=======

This project was inspired by [Scotch Box](https://box.scotch.io/) and built using the [Scotch Box Pro](https://box.scotch.io/pro/) build scripts by [Nicholas Cerminara](https://twitter.com/whatnicktweets). If you like this project, please also consider supporting Nick by purchasing a Scotch Box Pro license at a mere $15.

What's included?
================

Base Web Server Stack (LAMP)
----------------------------

1. Ubuntu 16.04 LTS
1. Apache 2
1. MySQL 5.7
1. PHP 7.0

Utilities
---------

1. Git
1. Vim
1. Imagemagick
1. Curl

Additional Software
-------------------

1. [PHPUnit](PHPUnit)
1. [PHPMyadmin](https://www.phpmyadmin.net/)
1. [Composer](https://getcomposer.org/)
1. [WP-CLI](http://wp-cli.org/)
1. [Ngrok](https://ngrok.com/)
1. [Node.js](https://nodejs.org/en/)
1. [Memcached](https://memcached.org/)
1. [Go](https://golang.org/)
1. [MailHog](https://github.com/mailhog/MailHog)

Configuration options
=====================

1. Ability to enable/disable update checks (when working offline)
1. Edit sitename, IP address and MySQL root password
1. Set Virtual Machine memory size
1. Automatically create info.php file in webroot

Requirements
============

1. [Vagrant]
1. [VirtualBox]
    
Initial Setup (Linux/OSx)
=======================
    
From your terminal window:    
    
Clone the repo to some place on your computer

```bash
git clone git@github.com:jonathanbossenger/boss-box-lamp.git
```

Switch to the boss-box-lamp directory

```bash
cd boss-box-lamp
```

Copy the 'vagrant' folder to your project web root

```bash
cp -r vagrant/ /path/to/myproject/webroot/vagrant/
```

Switch to the project vagrant directory

```bash
cd ~/path/to/myproject/webroot/vagrant/
```

Edit the settings.yaml file in the newly copied /path/to/myproject/webroot/vagrant/ directory as required.

Start BossBox        
        
```bash
vagrant up
```

How do I...
===========

**SSH into the Virtual Machine?**

From the terminal window

```bash
cd /path/to/myproject/webroot/vagrant/
vagrant ssh
```

**Access the development site?**
 
Browse to either the ip address or sitename you have specified in your settings.yaml

eg http://192.168.33.10 or http://sitename

**Access PHPMyAdmin?**

http://192.168.33.10/phpmyadmin or http://sitename/phpmyadmin

**Access MailHog?**

http://192.168.33.10:8025 or http://sitename:8025

http://wpjobs:8025



How to use? (Windows)
=====================

Coming soon

Setting hosts records
=====================

I recommend installing the [Vagrant Hosts Updater](https://github.com/cogitatio/vagrant-hostsupdater) plugin to allow your system to manage writing to the hosts file automatically.

```bash
vagrant plugin install vagrant-hostsupdater
```

Enjoy!    
    
