# Udacity - Linux Server Configuration
This project is for Udacity Full-Stack Developer course, the last project, and it has information to Udacity reviewer about an ubuntu instance in the Amazon Lightsail providing a basic Python application deployed over Linux, Apache, and PostgreSQL.

## How to login

Install the private key and run this:

    ssh -p 2200 grader@klassmann.link -i ~/.ssh/id_private_key

## Configuration Check-list
- [X] [Add the `grader` user in the system](https://www.linode.com/docs/security/securing-your-server/#ubuntu)
- [X] [`grader` user has `sudo` permission](https://www.linode.com/docs/security/securing-your-server/#ubuntu)
- [X] [`grader` user uses SSH key pairs for login](https://www.linode.com/docs/security/securing-your-server/#create-an-authentication-key-pair)
- [X] [Disabling SSH login with `root` user](https://www.linode.com/docs/security/securing-your-server/#ssh-daemon-options)
- [X] `SSH` has a non-standard port number
```
    Change this option in /etc/ssh/sshd_config:
    Port 2200
```
- [X] Only `SSH`, `HTTP` and `NTP` ports are configured in the firewall
```
    Use ufw with these options:

    $ sudo ufw default deny incoming
    $ sudo ufw default allow outgoing
    $ sudo ufw allow 2200/tcp
    $ sudo ufw allow www
    $ sudo ufw allow ntp
    $ sudo ufw enable
    
```
- [X] [It is allowed `SSH` login only with `RSA` key authentication](https://www.linode.com/docs/security/securing-your-server/#ssh-daemon-options)
- [X] All packages are updated in the operating system
```
    $ sudo apt-get update
    $ sudo apt-get upgrade
```
- [X] There is a web server running in the `80` port
```
    $ sudo apt-get install apache2 libapache2-mod-wsgi-py3
```

- [X] [There is a database configured and running](http://docs.sqlalchemy.org/en/latest/dialects/postgresql.html)
```
    $ sudo apt-get install postgresql
```
- [X] [The project `catalog` is running in the web server](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/#mod-wsgi-apache)

## Access information
In the browser use the address http://klassmann.link because the `catalog` app is configured with this domain in the Google OAuth.

- IP: 18.188.174.98
- URL: http://klassmann.link (unavailable)
- User name: `grader`
- Password: (It was sent directly to Udacity reviewer)
- Private Key: (It was sent directly to Udacity reviewer)

## Software list on the system
- [X] finger
- [X] Python 3.5
- [X] pip3
- [X] virtualenv
- [X] Apache2
- [X] mod_wsgi-py3
- [X] git
- [X] PostgreSQL 10

## Applications running
- [X] [Catalog](https://github.com/klassmann/udacity-catalog)

Requirements:
```
    Flask==0.12.2
    SQLAlchemy==1.2.5
    google-api-python-client==1.6.6
    google-auth==1.4.1
    google-auth-httplib2==0.0.3
    google-auth-oauthlib==0.2.0
    oauth2client==4.1.2
    oauthlib==2.0.7
```

## Third-Party Services
- [Amazon Lightsail](https://aws.amazon.com/lightsail/)
- [Amazon Route53](https://aws.amazon.com/route53/)

## License
You can't use this project as your project for Udacity, but you can use for study purposes if you want.
