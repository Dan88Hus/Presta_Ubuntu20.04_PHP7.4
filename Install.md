under sudo account

```
apt install mysql-server php apache2

```


```
sudo apt install php7.4-common php7.4-mysql php7.4-xml php7.4-curl php7.4-gd php7.4-cli php7.4-mbstring php7.4-zip php7.4-intl php7.4-json
```
```
  mysql -uroot
```
```
  CREATE DATABASE devHus;
 ```
 ```
  CREATE USER 'devHus'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
 ```
```
  GRANT ALL PRIVILEGES ON prestashop.* TO 'devHus'@'localhost';
```
```
  FLUSH PRIVILEGES;
```

cd /var/www/html/ can be changeaable 

```
wget https://download.prestashop.com/download/releases/prestashop_1.7.6.7.zip
```

mkdir prestashop
```
apt-get install php-zip php-simplexml
```
optionally
```
And THEN you have to add it manually to /etc/php/7.0/apache2/php.ini (apache2 or whatever web server you're using).

 

Just add those two lines at the end of the file :

extension=simplexml.so
extension=zip.so
```
systemctl restart apache2

a2enmod rewrite

source: 

https://www.youtube.com/watch?v=eQoJufGAZHc&list=PLvW0hHyu2_mrkDd8HxO15jnImoj1ygD5q&index=1&t=79s
