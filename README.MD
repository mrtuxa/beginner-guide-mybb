This is a guide on how to install and how to configure MyBB Forum. 

Step 1.

Installing phpmyadmin with this script.


For Ubuntu
```bash
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall-ubuntu/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

For Debian

```
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

Step 2: Downloading the mybb archive

``
cd /var/www/html
``

``
wget https://resources.mybb.com/downloads/mybb_1829.zip
``

``
unzip mybb_1829.zip
``

``
rm -rvf Documentation
``

``
mv -v Upload forum
``

``
cd forum
``

``
mv inc/config.default.php inc/config.php
``

``
chmod 666 inc/config.php inc/settings.php
``

``
chmod 777 cache/ cache/themes/ uploads/ uploads/avatars/
``

``
chmod 666 inc/languages/english/*.php inc/languages/english/admin/*.php
``

``
chmod 777 cache/ cache/themes/ uploads/ uploads/avatars/ admin/backups/
``

Step 3: Create the database user and database table

``
mysql -u root
``

```
root@mysql:~# mysql -u root -p
Enter password:

Welcome to the MySQL monitor. Commands end with ; or \g.
Your MySQL connection ID is 98
Server version: 5.5.47-0+deb8u1 (Debian)

Copyright (c) 2000, 2015, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```

this will show up, then u need to run this command exactly as shown, but with your own data

``
CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';
``

``
CREATE DATABASE 'forum';
``

``
GRANT ALL PRIVILEGES ON forum . * TO 'user'@'localhost';
``

``
FLUSH PRIVILEGES;
``

Step 4: configure everything what the installer wants to know,
        after configuring you need to type in the last command.
        
``
cd /var/www/html/forum
``

``
rm -rvf installation
``
