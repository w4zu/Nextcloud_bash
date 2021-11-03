# Nextcloud_bash
Its a bash script to install Nextcloud and lot of apps.

## Required
Lamp complete installation : Linux (Debian) , Apache, PHP 7.3+, Mariadb or mysql , python3

## What the script does
The script will check if php/mysql are installed and install certbot.
This script install redis-server for nextcloud cache and 6 php packets, it also enables http2 support for apache2.
Apache vhosts will be created on /etc/apache2/sites-enabled, and a sql database.
Download Nextcloud version and install on document root.
Then several configuration and optimization of the nextcloud configuration are done directly from nextcloud command line.
## Before lunch this script 
Variables to changes before use this script : 

phpversion=8.0 # PHPversion do you want, 8.0 is the default but you can use 7.3.
ncversion=22 # Version of nextcloud do you want 22 is a default
domain="cloud.yourdomain.org" # Domain used for the nextcloud application, it must point to the server.
admin_mail="youremail@domain.org" # Your email used for SSL certificates and postmaster for vhost apache.
username=www-data # This is the user who has to launch the application with PHP 
mydocroot="/var/www/$username/" # This is where nextcloud is installed.
myvhost="/etc/apache2/sites-enabled/nextcloud_$domain.conf" # Its apache2 file configuration by default.
hostsql="localhost" # IP of your mysql server

