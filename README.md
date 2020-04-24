![Repo Image](https://github.com/lalantham/install-wordpress/blob/master/img.jpg)
# Install Wordpress In Linux (Ubuntu)

>Complete Guild for install wordpress in linux 

## 01 - Install Wordpress Localy

	1.1 - Download wordpress zip file
		https://wordpress.org/download/

	1.2 - Extract and Place wordpress file in to whatever location you want		  

	1.3 - Install apache modules for permalinks
          sudo a2enmod rewrite
          
	1.4 - Create virtual host for wordpress
		  <VirtualHost *:80>
			    ServerName whatever.name
			    DocumentRoot /path to wordpress folder

			    <Diretory />
				      Options FollowSymLinks
				      AllowOveride All
			    </Directory>

			    <Diretory /path to wordpress file>
				      Options Indexes FollowSymLinks
				      AllowOverride All
				      Order allow,deny
				      allow from all
			    </Directory>
		  </VirtualHost>
          
	1.4 - Enable Wordpress site
		sudo a2ensite name of conf file

	1.5 - Enable Virtual Server
		sudo a2ensite conf file name 'whatever.name.conf'

	1.6 - Restart Apache2
		sudo service apache2 restart , sudo systemctl reload apache2

	1.7 - Edit Hosts
          	Add entry wordpress entry under localhost ip in /etc/hosts

## 02 - Database

	2.1 - Make Database for wordpress
		Using termianl or any gui client

## 03 - Wordpress Installation

	3.1 - Error - Cant write the wp-config.php file
		  Copy the code in box
		  make wp-config.php file in wordpress folder
        3.2 - Error - .htaccess
		  Create file in wordpress file
		  Add .htaccess code in wordpress dashboard
