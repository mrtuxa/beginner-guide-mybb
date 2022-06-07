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
wget https://resources.mybb.com/downloads/mybb_1830.zip
``

``
unzip mybb_1830.zip
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

// german

1. Schritt

Installation von phpmyadmin mit diesem Skript.


Für Ubuntu
```bash
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall-ubuntu/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

Für Debian

```
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

2. Schritt :  Herunterladen des mybb-Archivs

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

3. Schritt : Anlegen des Datenbankbenutzers und der Datenbanktabelle

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

dies wird angezeigt, dann müssen Sie diesen Befehl genau wie gezeigt ausführen, aber mit Ihren eigenen Daten

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

4. Schritt :    konfigurieren Sie alles, was das Installationsprogramm wissen will,
                nach dem Konfigurieren müssen Sie den letzten Befehl eingeben.
        
``
cd /var/www/html/forum
``

``
rm -rvf installation
``

// japanese

MyBB Forumのインストール方法と設定方法について説明します。

ステップ1

このスクリプトでphpmyadminをインストールする。


Ubuntuの場合
```bash
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall-ubuntu/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

Debianの場合

```
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

ステップ2：mybbアーカイブのダウンロード

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

ステップ3：データベースユーザーとデータベーステーブルの作成

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

が表示されたら、表示されたとおりに、自分のデータを使ってこのコマンドを実行する必要があります。

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

ステップ4：インストーラが知りたがっていることをすべて設定する。
        設定後、最後のコマンドを入力する必要があります。
        
``
cd /var/www/html/forum
``

``
rm -rvf installation
``

// chinese (simplified)

这是一份关于如何安装和如何配置MyBB论坛的指南。


步骤1。

用这个脚本安装phpmyadmin。


对于Ubuntu
```bash
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall-ubuntu/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

对于 Debian

```
wget https://raw.githubusercontent.com/mrtuxa/mariadbautomaticinstall/main/phpmyadmin.sh; chmod +x phpmyadmin.sh; bash phpmyadmin.sh
```

第2步：下载mybb档案

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

第3步：创建数据库用户和数据库表

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

这将显示出来，然后你需要运行这个命令，完全如图所示，但使用你自己的数据

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

第4步：配置安装程序想知道的一切。
        配置完毕后，你需要输入最后一条命令。
        
``
cd /var/www/html/forum
``

``
rm -rvf installation
``
