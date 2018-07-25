# Linux Server Configuration Project

Resources and info about the project.

## Project

Baseline installation of a Linux distribution on a virtual machine prepared to host a web application, including installing updates, security from a number of attack vectors and installing/configuring web and database servers.
This project makes part of the [Full-Stack Web Nanodegree Program](https://udacity.com/course/full-stack-web-developer-nanodegree--nd004) from Udacity.

## Details about the installation

* IP address and SSH port: 52.15.106.140 2200
* Complete URL to your hosted web application: http://52.15.106.140:5000/
* Summary of software you installed and configuration changes made:
  * Installed software: apache, postgresql, git, python3 and flask plus some plugins.
  * Configurated firewall to allow the following ports: 80, 2200 and 5000.
  * See below the main executed commands.

```sh

    sudo apt-get update
    sudo apt-get upgrade
    sudo ufw default deny incoming
    sudo ufw default allow outgoing
    sudo ufw allow 2200/tcp
    sudo ufw allow ssh
    sudo ufw allow www
    sudo ufw allow ntp
    sudo apt-get install apache2
    sudo apt-get install libapache2-mod-wsgi
    sudo nano /etc/apache2/sites-enabled/000-default.conf
    sudo apt-get install libapache2-mod-wsgi-py3
    sudo apt-get install postgresql
    sudo apt-get install git
    sudo apt install python3-pip
    pip3 install Flask
    pip3 install Flask-Babel
    pip3 install flask-sqlalchemy
    pip3 install flask-marshmallow
    pip3 install -U flask-sqlalchemy marshmallow-sqlalchemy
    pip3 install Flask-WTF
    pip3 install Flask-OAuthlib
    pip3 install --upgrade oauth2client
    cd /var/www/html/item-catalog-project/
    flask run --host=0.0.0.0 --port=5000
```

* List of any third-party resources you made use of to complete this project:
  * No third-party resource is used.
* Locate the SSH key you created for the grader user: /home/grader/.ssh/authorized_keys

## License

All the code in this project is a public domain work, dedicated using [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). Feel free to do whatever you want with it.