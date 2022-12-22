# Multicraft

For Forge servers:

Installer configs - Update config & jar.

Non-installer configs - Update config ONLY.


In the servers settings Look for JARs in Server base directory.


Run server with the forge installer, this will run the forge installer jar with the --installServer argument.


After it's successful stop the server, change the jar to the non-installer and run the server like normal.

When updating or changing jars, make sure you delete all forge files including the forge jar, minecraft_server jar and libraries directory.


To install Java 8, 16 and 17 on Ubuntu use ```sudo apt update -y && sudo apt upgrade -y && sudo apt install openjdk-8-jre-headless openjdk-17-jre-headless openjdk-18-jre-headless -y``` This will update and up grade your machine then install the java versions without any confirmation, if you want to confirm each action, remove the ```-y``` from each section.

If you would like a certain jar config file please let me know.
