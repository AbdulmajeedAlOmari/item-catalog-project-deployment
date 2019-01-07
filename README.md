# Item Catalog Project Deployment
You will take a baseline installation of a Linux server and prepare it to host your web applications. You will secure your server from a number of attack vectors, install and configure a database server, and deploy one of your existing web applications onto it.

_This project is required for Full-Stack Nanodegree program._

## What I used to deploy my application
- [Lightsail](lightsail.aws.amazon.com) server
- Used terminal to access my server using SSH
- [Apache2](https://httpd.apache.org/)

## Server Information
- **IP**: `3.120.188.179`
- **SSH Port**: `2200`
- **Website Home Page**: http://3.120.188.179.xip.io/catalog

## Summary of Software Installed
- `libapache2-mod-wsgi-py3`.
- [PostgreSQL](https://www.postgresql.org/).
- `Git`.
- [Python3](https://www.python.org/).
- `pip3` (to install python3 modules).
- Installed all modules used by `item-catalog` application.

## Summary of Configuration Changes
- Updated all the installed packages.
- Changed default SSH port from `22` to `2200`.
- Disabled access using passwords.
- Modified Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
- Created a user named as `grader` to allow the reviewer to access the server.
- Created an SSH key pair for `grader` using `ssh-keygen` tool.
- Created a new user named as `catalog` to have access to the database.
- Created a Virtual Host for the item-catalog application.
- Modified Item Catalog application apache configurations in the file `ItemCatalog.conf`.
- Created `itemcatalog.wsgi` file to allow connection between my Python application and Apache2.
- Updated `client_secret.json` to allow `xip.io` domain and to allow `3.120.188.179.xip.io` redirects.
- Added server name alias `3.120.188.179.xip.io` in `ItemCatalog.conf`.

## References
I used the following references to help me finish this project:
- [Installation of PostgreSQL](https://tecadmin.net/install-postgresql-server-on-ubuntu/)
- [How to add a PostgreSQL user](https://www.cyberciti.biz/faq/howto-add-postgresql-user-account/)
- [Installation of pip3](https://www.tecmint.com/install-pip-in-linux/)
- [Connecting to PostgreSQL database](https://docs.sqlalchemy.org/en/latest/core/engines.html)
- [Deploying flask application](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
