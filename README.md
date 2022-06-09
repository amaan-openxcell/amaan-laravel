sudo apt-get update
git clone https://github.com/ozdemirburak/laravel-8-simple-cms.git && cd laravel-8-simple-cms {link from git}
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
sudo apt -y install php7.4
sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath
sudo wget https://getcomposer.org/download/2.3.7/composer.phar
sudo composer self-update 1.10.12
sudo mv composer.phar /usr/local/bin/composer
sudo chmod +x /usr/local/bin/composer
sudo composer install
composer --version
php -v
sudo apt install -y mariadb-server
sudo apt install -y apache2
sudo mysql -u root -p
    CREATE DATABASE amaan_khan;
    CREATE USER 'amaan'@'localhost' IDENTIFIED BY 'password';
    GRANT ALL ON amaan_khan.* TO 'amaan'@'localhost';
    FLUSH PRIVILEGES;
    QUIT;
sudo vim .env
    *database_name*
    *user_name*
    *password*
sudo systemctl restart mariadb
sudo systemctl restart apache2
sudo php artisan cms:initialize --seed
php artisan serve