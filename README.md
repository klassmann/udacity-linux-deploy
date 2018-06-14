# Udacity - Linux Server Configuration
This project is for Udacity Full-Stack Developer course, the last project, and it has information to Udacity reviewer about an ubuntu instance in the Amazon Lightsail providing a basic Python application deployed over Linux, Apache, PostgreSQL.

## How to login

Install the private key and run this:

    ssh -p 2200 grader@tierw.com -i ~/.ssh/id_private_key

## Configuration Check-list
- [X] Add the `grader` user in the system
- [X] `grader` user uses SSH key pairs for login
- [X] `grader` user has `sudo` permission
- [X] Disabling SSH login with `root` user
- [X] Only `SSH`, `HTTP` and `NTP` ports are configured in the firewall
- [X] `SSH` has a non-standard port number
- [X] It is allowed `SSH` login only with `RSA` key authentication
- [X] All packages are updated in the operating system
- [X] There is a web server running in the `80` port
- [X] There is a database configured and running
- [X] The project `catalog` is running in the web server

## Access information
- IP: 18.188.174.98
- URL: http://klassmann.link
- User name: `grader`
- Password: (It was sent directly to Udacity reviewer)
- Private Key: (It was sent directly to Udacity reviewer)

## Software list on the system
- [X] finger
- [X] Python 3.5
- [X] pip3
- [X] virtualenv
- [X] Apache
- [X] mod_wsgi
- [X] git
- [X] PostgreSQL 10

## Applications running
- [X] [Catalog](https://github.com/klassmann/udacity-catalog)


## License
You can't use this project as your project for Udacity, but you can use for study purposes if you want.
