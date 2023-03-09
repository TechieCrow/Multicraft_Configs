# Readme
# Forge Stuff

For Forge servers:

Installer configs - Update config & jar.

Non-installer configs - Update config ONLY.


In the servers settings Look for JARs in Server base directory.


Run server with the forge installer, this will run the forge installer jar with the --installServer argument.


After its successful stop the server, change the jar to the non-installer and run the server like normal.

When updating or changing jars, make sure you delete all forge files including the forge jar, minecraft_server jar and libraries directory.

------------


# To Install Multicraft Dependences & Java 8, 17 and 18
```sudo apt update -y && sudo apt upgrade -y && sudo apt install apache2 php libapache2-mod-php php-mysql php-gd php-sqlite3 openjdk-8-jre-headless openjdk-17-jre-headless openjdk-18-jre-headless -y```

```sudo mkdir /var/www/your_domain```

```sudo chown -R $USER:$USER /var/www/your_domain```

```sudo vim /etc/apache2/sites-available/your_domain.conf```


    <VirtualHost *:80>
        ServerName your_domain
        ServerAlias www.your_domain
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/your_domain
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>


```sudo a2ensite your_domain```

```sudo a2dissite 000-default```

```sudo apache2ctl configtest```

```sudo systemctl reload apache2```

```sudo vim /etc/apache2/mods-enabled/dir.conf```

```sudo systemctl reload apache2```

```sudo a2enmod rewrite```

```sudo systemctl reload apache2```

This will update and upgrade your machine then install all of multicrafts dependences as well as the java versions without any confirmation.

To actually install MultiCraft itself, please look at their docs on their website.

If you would like a certain jar config file please let me know.
