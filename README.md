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


# To Install Multicraft Dependences & Java 8, 17 and 21
I am using ansible to automate the dependences, I'm still very new to ansible so please make sure you read all the files before using them.

To actually install MultiCraft itself, please look at their docs on their website.

```Download the files in Multicraft-Setup and run the setup_multicraft.yml ansible playbook, it will install all the required dependences, setup mysql, phpmyadmin and an apache2 vhost for the panel```
```Please change these:
In setup_vhost.yml:
	site_name: "website-directory"
	server_admin: "email"

In setup_mysql.yml:
	mysql_root_password: "database-password
	
In setup_certbot.yml:
	domain_name: "panel-domain"
    email_address: "email"
