## Quick Start:
First Update Your System.

    $ sudo apt-get update



Clone this repository and install the dependencies.

    $ git clone https://github.com/ozdemirburak/laravel-8-simple-cms.git && cd laravel-8-simple-cms
    $ composer install


Installing php with this repo.
    
    $ sudo add-apt-repository ppa:ondrej/php
    $ sudo apt-get update
    $ sudo apt -y install php7.4
    $ sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath



Downloading "composer"

    $ sudo wget https://getcomposer.org/download/2.3.7/composer.phar
    
    
Downgrading composer.
   
    $ sudo composer self-update 1.10.12


Making cmposer global.
    
    $ sudo mv composer.phar /usr/local/bin/composer
    $sudo chmod +x /usr/local/bin/composer


Installing "composer"

    $ sudo composer install


Checking "composer" version.
    $ composer --version
    $ php -v


Installing mariadb [Databse].

    $ sudo apt install -y mariadb-server


Installing WebServer.

    $ sudo apt install -y apache2


Once the database server is installed, log into the MariaDB prompt:

    $ sudo mysql -u root -p
    
    
Once logged in create the database, database user, and grant all privileges to the database user:
    
    CREATE DATABASE amaan_khan;
    
    CREATE USER 'amaan'@'localhost' IDENTIFIED BY 'password';
    
    GRANT ALL ON amaan_khan.* TO 'amaan'@'localhost';
    
    FLUSH PRIVILEGES;
    
    QUIT;



Updating .env file.

    $ sudo vim .env
        *database_name*
        *user_name*
        *password*



Restarting Service.

    $ sudo systemctl restart mariadb
    $ sudo systemctl restart apache2


Staring Application;
    
    $ sudo php artisan cms:initialize --seed
    $ php artisan serve
