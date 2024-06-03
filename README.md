# Multicraft Configuration and Setup

This repository contains my personal `jar.config` files for Multicraft and Ansible playbooks to streamline the setup process on a new server.

## Forge Server Configuration

Note: I will not be adding or updating anymore Forge jar.conf files, they are annoying to setup, maintain and honestly a lot of the hybrid server software is good enough to run only Forge mods now, if you want an updated Forge jar.conf you can use my files as a base for your own.

### For Forge Servers:
1. **Installer Configs**: Update the config and JAR files.
2. **Non-installer Configs**: Update the config only.

**Steps:**
1. In server settings, set "Look for JARs in Server base directory".
2. Run the server with the Forge installer (`--installServer` argument).
3. After successful installation, stop the server.
4. Switch to the non-installer JAR and run the server normally.

**Note:** When updating or changing JARs, delete all Forge files including the Forge JAR, `minecraft_server` JAR, and the `libraries` directory.

## Installing Multicraft Dependencies & Java (8, 17, 21)

Use Ansible to automate the installation of dependencies. Ensure you review all files before use as this is a work in progress.

### Instructions:
1. Download files in `Multicraft-Setup`.
2. Run `setup_multicraft.yml` playbook. This will install dependencies, set up MySQL, phpMyAdmin, and an Apache2 vhost for the panel.

### Ansible Configuration:
- **setup_vhost.yml**:
  ```yaml
  site_name: "website-directory"
  server_admin: "email"
- **setup_mysql.yml**:
  ```yaml
  mysql_root_password: "database-password"
- **setup_certbot.yml**:
  ```yaml
  domain_name: "panel-domain"
  email_address: "email"
  
### About:
This repository includes my custom jar.config files for Multicraft.
