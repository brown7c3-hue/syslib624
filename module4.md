# Intro

LAMP stands for Linux, Apache, MySQL and PHP. A LAMP stack involves open source software that is used in the creation of websites and applications like WordPress and Koha. The only problems I encountered during this unit were user-error. I kept missing punctuation marks and making typos, which I can try to do better with moving forward by slowing down and double checking my work before entering any commands. 

## Apache

**Installation**

1. sudo apt update
2. sudo apt -y upgrade
3. apt search apache2 | head
4. apt show apache2
5. sudo apt install apache2

**Configuration**

For the text based browser, I installed w3m. I viewed the default web page from Chrome by using my server’s public IP address from Google Cloud. I created the web page with the following commands: 

```
cd /var/www/html/
sudo mv index.html index.original.html
sudo nano index.html
```

**Verifying**

I used the systemctl command to confirm that apache2 was running correctly. 

## PHP

**Installation**

1. sudo apt install php libapache2-mod-php
2. sudo systemctl restart apache2
3. php -v

**Configuration**

```
cd /etc/apache2/mods-available/
sudo cp dir.conf dir.conf.bak
sudo nano dir.conf
DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
sudo systemctl reload apache2
systemctl status apache2
```

**Verifying**

I used the systemctl status apache command to check for any errors in the log output after the php -v command. I verified PHP was installed correctly and that it was working with Apache by changing the directory to the document root (/var/www/html/) and created a nano file titled info.php. To confirm PHP is installed correctly, I opened my public IP address in my chosen browser (Chrome), and I saw the PHP title at the top of my screen. 

## MySQL

**Installation**

1. sudo apt update
2. sudo apt upgrade
3. sudo apt autoremove
4. sudo apt clean
5. sudo apt install mysql-server
6. apt policy mysql-server
7. mysql --version
8. systemctl status mysql

**Configuration**

```
sudo mysql_secure_installation
* Validate passwords: Y
* Password validation policy: 0 (zero) for LOW
* Remove anonymous users: Y
* Disallow root login remotely: Y
* Remove test database and access to it: Y
* Reload privilege tables now: Y
sudo mysql -u root
mysql> show databases;
mysql> \q
```

**Verifying**

To verify each component is working, I used the systemctl command and looked at the lines that started with “loaded” and “active.” I used the “show” and “describe” commands to confirm the table was created once I got to that point. Lastly, I used the following commands to test the PHP syntax for any errors:

```
sudo php -f /var/www/login.php
sudo php -f /var/www/html/opac.php
```
