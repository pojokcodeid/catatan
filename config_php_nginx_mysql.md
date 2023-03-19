sudo apt-get update && sudo apt-get upgrade -y
sudo add-apt-repository ppa:nginx/stable
sudo apt-get update
sudo apt-get install nginx -y
sudo service nginx start

sudo ufw app list
sudo uff allow OpenSSH
sudo ufw allow 'Nginx Full'

sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
sudo apt-cache show php
sudo apt-get install php8.2-cli php8.2-fpm php8.2-curl php8.2-gd php8.2-mysql php8.2-mbstring zip unzip

sudo service php8.2-fpm start

sudo nano /etc/nginx/sites-available/default
-- tambahkan index.php 

location ~ \.php$ {
    include snippets/fastcgi-php.conf;
    fastcgi_pass unix:/run/php/php8.2-fpm.sock;
}

-- buat alias di home dir
sudo ln -s /var/www/pcode /home/asep/pcode 

# Install MySQL
```
sudo apt-get install mysql-server
mysql --version
sudo /etc/init.d/mysql start
sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED with mysql_native_password BY 'password';
FLUSH PRIVILEGES;

exit
sudo mysql_secure_installation -p
n 
n 
y
n 
n
y
```
- test login
```
sudo mysql -u root -p
```
- Edit Port
```
sudo nano /etc/mysql/my.cnf
```
- tambahkan pada paling bawah
```
[mysqld]
port = 33061
```
- restart MySQL
```
sudo service mysql restart
sudo update-rc.d mysql defaults
```
- Test koneksi dari host Windows
