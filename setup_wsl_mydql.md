set user root
visudo
[nama user] ALL=(ALL:ALL) ALL
[nama user] ALL=(ALL) NOPASSWD:ALL

sudo apt-get update && sudo apt-get upgrade
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

sudo mysql -u root -p

sudo nano /etc/mysql/my.cnf

- tambahkan code port paling bawah
[mysqld]
port = 33061

sudo service mysql restart
sudo update-rc.d mysql defaults
- selanjutnya test koneksi menggunakan dbeaver dari windows
