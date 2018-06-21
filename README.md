# Linux-Server-Configuration
About
This Project is about configuring the Linux-Server.

Server Details
Server IP Address 13.126.118.92

Hosted site Url http://13.126.118.92.xip.io/

How to connect as grader:
save private key provided in your local machine and run the following command

ssh -i path/to/privatekey -p 2200 grader@13.126.118.92
  
Id_rsa key
-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEA1FpQHw36n6DHPviYo0T+8X0BurkCH7s5Z3zcgnXV9wFYw4uQ
xPJ/vsDRBzfY5kLv3OmqV4DiehLXXGBUNBiVECuBxa6Mt4pHSyPpq+2zY7XZ94jC
tRsAxOH9wO7OmDY4Rmx1yInf2+sNiCk/5VWA/z6f6KjCVqJtum5IEcLdmnfgrEFS
+xGvJ6l9+dYPlD4pyIPINt2DC0VV67UsMscAMfz2/wJj+t8e/4YvhC+TBgZXCoOA
xiT/KzqjRggkyFW2zkEcFPLH7dt9u7Ss5jrPHLBJq09gcuj8klUyQhHqxaHpU2zH
5runCPwcsK0UWHqBi4Oi+rY3nWzbYHYkX0kUKQIDAQABAoIBAGHmOSX4BeFt+C25
4nTzLC4dGZ0CCk6ivDZPxEGJHdnAjzGnuFh0DBzfO/796ktN9NN+DoBE9SSeZxc5
ediCtMY9qJiAfnNnlrK3ndUbwyZnAlQygsGH73TVU22NK0XVSWB+RFbt6Xy0AwsR
KVoLb2s9be+PTfku7TOUADngAtZhMkla/7TK7QKU/4LGhm3m2qKldq0zkDtN1CLZ
XaWuDyGxhAqU7eA1aY1w69/pIthOgIAFFznCZ45CbYvH/Jvg7/mEqhFsqZ5h687v
8KO8oehVVaGjMF1xd3r3DQ8t3QfpRaVauUAS4odfOLc7IkLKcf834qhrio6ffnmo
x/EDoWECgYEA/QWk5yFgiXtrtrC6vgeuJSMaQN9igJelWQ1ppcrW2XwUZrhjl2zX
d4234wShajFzSs/shVp7eWoJcNiz56oRMJfINwKwMbPnlnasfFlnlrTPcT0k/1AX
53dzajJ9Sa32f8fDMFgJS42gOhV0YB1TM1ZAQZqtrS5SE/b8odEVWR0CgYEA1toh
3EDnRg91diasLYkg7xhnzlJtupgb1RLqeOiGdBZOu2KW7qyJ0RK4El3+fJkd/xMT
Xt5As58L6vtbDDJnMlPIdXLcodNMj+gnffpnF5/bTfDt4gmI+GUq9AQrEnqHWvvb
fgNrC1wp8fjqgOcltLdKCoZ/pPg/FZ+9ybZrBX0CgYB2jlJ6SlVllgMekyitKgQb
Optukj0ha+z6ESLToHuTZGRazUM9DK7ZQfpL0Tug+pK/FzYINiFs/pZ13dROVI3B
ax1RSV0trNJy2iBwE6RKJWad9LyFNQ4+UuYteILkJzM9JGj9GgMg97d//9WLw7Hc
eCmbk9KVNwMWf8BYQhPysQKBgBRUNWn6tidZ5RpV1GrGk9grrf7Gq91A8Tk6/faM
wdQQHEj8rh1NNAkVRVdvj1nIvx7Ydje+vc6BGQaV2+qOhlcruEbspFWngZIIPFxe
Kg0BMiXwywFdN5mRMPw/vLeV4mLIe98zgZhkkw9zJvUladrskNPoIAHC/20TXUjN
utidAoGBAM7RasVZDUbqUtrzxInKdZ10LhWsQ4qEeet4o+irz09+nD8RgMK4jtKc
47caNTbtqiTyHqQrRFpKO/SMriDlyUqqjIRSanZO+HjfNG43MVsjPbyAJUkjlVVv
K/mIhgTXdPlU5s4mE+UbewL958EdBZawDTX2zZxqLbjf8XJX1Lkl
-----END RSA PRIVATE KEY-----


passpharse password
''' passpharse password is empty(you can directly press enter).

'''

id_rsa.pub key
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDkHVXGXVykGS7+l4WrjcDm6uDPdiN2a6LVuNgrbeLWkxsn6W/KjKhB83wz8/b0TNVbHrQb/i75knswYXvLNeJDINHTVbUIoQdJAdpLf+aRsaOzhQVSExRGYbmlM+8HUGKPKsuKCOkzgeF20Lcu+cR4XGgzNdYJAmR+oG9X6Rhx14Q1uN/CAaQxQw6u05lRIJfVmzR9tfc/+7Ii/Tepf7TqVsXcMdJy/q1YBluOmGfM5KMXui2paJKMrpV/DfIt3W3FV1qbopuuo0ay6jqnoTkTl9xmCzpkabD0Cg28aSSNq+GlAE9/gFCiNwR4TjT2R0MSFLMEBRwMsiC82CcLnYLp sree@DESKTOP-LUNCTQ2


grader password
unix
Configuring Linux Server
Updating all packages
sudo apt-get update
sudo apt-get upgrade
Creating grader User:
sudo adduser grader
This will add new user

sudo nano /etc/sudoers
Below the Root user append the following line

grader  ALL=(ALL:ALL) ALL
This will grant sudo permission to grader

Creating a ssh key pair for grader
On your local machine in terminal/command prompt type

ssh-keygen
Which will generate the public and private ssh keys which is saved to .ssh folder

Then in your virtual machine change to newly created user

su - grader
Create a new directory .ssh and new file authorized_keys in that directory

mkdir .ssh
sudo nano .ssh/authorized_keys
Copy the public key with .pub extension to authorized_keys and save the file

chmod 700 .ssh
chmod 644 .ssh/authorized_keys
700 will give read write and execute permission to user.
644 prevent other user from writting in to file. Then restart ssh server
service ssh restart
Log in to grader with private key generated

ssh -i .ssh/id_rsa grader@ipaddress 
Changing the ssh port to 2200
sudo nano /etc/ssh/sshd_config
Restart the ssh server

service ssh restart
Note: Before Logging using ssh add custom TCP port 2200 under lightsaail firewall in networking tab in lightsail instance console

Now Login using command like this

ssh -i .ssh/id_rsa -p 2200 grader@youripaddress
Disabling ssh login as root
sudo nano /etc/ssh/sshd_config

make change PermitRootLogin no

Configurating Ufw firewall
sudo ufw status
sudo ufw allow 2200/tcp
sudo ufw allow 80/tcp
sudo ufw allow 123/udp
sudo ufw enable
This will allow all required ports and enables the ufw

sudo ufw status
It will display all allowed ports

Changing time Zone
sudo dpkg-reconfigure tzdata

select none from list and then select utc.

Installing Apache2
In terminal

sudo apt-get install apache2

Now mod_wsgi

sudo apt-get install python-setuptools libapache2-mod-wsgi

Enable mod_wsgi

sudo a2enmod wsgi

Setting up your flask application to work with apache2
Creating a flask app

In /var/www directory create a new folder sudo mkdir FlaskApp

Install git

sudo apt-get install git

move to the FlaskApp cd FlaskApp

In that direcory clone your github repository

sudo git clone https://github.com/username/catalog.git

Rename your repository to FlaskApp

Then rename your project file to __init__.py

Error : While accesssing the client_secrets.json file

PROJECT_ROOT = os.path.realpath(os.path.dirname(__file__))
json_url = os.path.join(PROJECT_ROOT, 'client_secrets.json')
CLIENT_ID = json.load(open(json_url))['web']['client_id']
Use json_url instead client_secrets.json in script

Install and configuring postgresql for project
Install Postgres sudo apt-get install postgresql

login to postgres sudo su - postgres

postgres shell psql

create user CREATE USER catalog WITH PASSWORD 'password';

permit user to createdb ALTER USER catalog CREATEDB;

Create a db name catalog with user catalog CREATE DATABASE catalog WITH OWNER catalog;

connect to db \c catalog

revoke all permission to public REVOKE ALL ON SCHEMA public FROM public;

Give schema permission to user catalog GRANT ALL ON SCHEMA public TO catalog;

exit from db and postgres \q and exit

Change the database connection in both db_setup.py and __init__.py as engine = create_engine('postgresql://catalog:password@localhost/catalog')

Now you are ready with your applicatiom

Configure and Enable a New Virtual Host
sudo nano /etc/apache2/sites-available/FlaskApp.conf

In this add the following code

<VirtualHost *:80>
 	ServerName mywebsite.com
 	ServerAdmin admin@mywebsite.com
 	WSGIScriptAlias / /var/www/FlaskApp/flaskapp.wsgi
 	<Directory /var/www/FlaskApp/FlaskApp/>
 		Order allow,deny
 		Allow from all
 	</Directory>
 	Alias /static /var/www/FlaskApp/FlaskApp/static
 	<Directory /var/www/FlaskApp/FlaskApp/static/>
 		Order allow,deny
 		Allow from all
 	</Directory>
 	ErrorLog ${APACHE_LOG_DIR}/error.log
 	LogLevel warn
 	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
Enable the virtual host sudo a2ensite FlaskApp

Disabling the default apache2 page sudo a2dissite 000-default.conf

Create the .wsgi File
```
cd /var/www/FlaskApp
sudo nano flaskapp.wsgi 
```
Add the following code

#!/usr/bin/python
 import sys
 import logging
 logging.basicConfig(stream=sys.stderr)
 sys.path.insert(0,"/var/www/FlaskApp/")

 from FlaskApp import app as application
 application.secret_key = 'Add your secret key'
save and exit

Deploying flask app with apache2 is referred from Digital ocean

Installing require modules
You can either install all modules on your machine or create a virtual environment for the project and install the modules pip install flask sqlalchemy psycopg2 requests oauth2client

Setting up your Google Oauth2
Login to your developer console and select your project and edit OAuth details as following

Javascript origin http://ip.xip.io

redirect URI

http://ip.xip.io/login

http://ip.xip.io/gconnect

http://ip.xip.io/callback

xip.io is a free DNS which will be the same as using IP address

Final Step
Restart your apache2 server

sudo service apache2 restart

Click here to Reply or Forward
