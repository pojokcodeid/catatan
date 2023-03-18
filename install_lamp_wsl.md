1. Install WSL ubuntu dari windows store 
2. create user akun
3. allow root
```
sudo visudo
[nama user] ALL=(ALL:ALL) ALL
[nama user] ALL=(ALL) NOPASSWD:ALL
```
4. Lakukan update system
```
sudo apt-get update && sudo apt-get upgrade -y
```
5. Install PHP dan Apache2
```
sudo apt-get install apache2 php libapache2-mod-php php-mysql -y
sudo service apache2 start
```
6. Allow acess folder
```
sudo chmod 777 /var/www/html -R
ln -s /var/www/html public_html
```
7. Create file php
```
cd public_html
vim index.php
```
