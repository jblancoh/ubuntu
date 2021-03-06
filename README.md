# Instalacion de algunas paqueterias

## Instalar Pycharm
sudo add-apt-repository ppa:mystic-mirage/pycharm
sudo apt-get update

#### Version Pro
sudo apt-get install pycharm
#### Desinstalar Pro
sudo apt-get remove pycharm

#### Version Community
sudo apt-get install pycharm-community
#### Desinstalar Community
sudo apt-get remove pycharm-community

#### Remover el repositorio
sudo add-apt-repository --remove ppa:mystic-mirage/pycharm

###Python
#### Instalar PIP (python3)
sudo apt-get install python3-pip
#### Instalar python3-dev (python3)
sudo apt-get install python3-dev
#### Psycopg2
pip install psycopg2


## 1 Postgres
#### Instalar Postgresql
sudo apt-get install postgresql
#### Instalar libpq-dev (para conectar django con postgres)
sudo apt-get install libpq-dev
#### Modificar template para modificacion de Pass 'postgres'
sudo su postgres -c "psql template1"
```
ALTER USER postgres WITH PASSWORD 'postgres';
```
## 2 Postgres
#### Instalar Postgresql
sudo apt-get install libpq-dev python-dev
#### Instalar libpq-dev (para conectar django con postgres)
sudo apt-get install postgresql postgresql-contrib

### Create the database
sudo su - postgres
$ psql
psql (9.3.4)
Type "help" for help.

CREATE USER name WITH PASSWORD 'password';
 
CREATE DATABASE djangogirls OWNER name;

### Install Django within a Virtual Environment
source myenv/bin/activate

pip install django psycopg2

virtualenv -p python3 envname


## NODEJS
#### Instala NVM
curl https://raw.githubusercontent.com/creationix/nvm/v0.10.0/install.sh | sh

Una ves que tengamos NVM es cuestión de utilizarlo en la terminal

- nvm ls Lista las versiones disponibles localmente
- nvm ls-remote Lista las versiones remotas, de esta manera sabras que puedes instalar
- nvm install < version > Instalara la version que le especifiques, o la mas cercana a ella.
- nvm use < version > Usara la version especificada como la version por default
- nvm run < version > app,js Correrá la aplicación que le indiquemos con esa version de Node.js

## ZSH
#### Instala zsh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"   

chsh -s $(which zsh)
#### Crear alias
atom ~/.zshrc   
alias e="atom"   
alias pro="cd ~/Projects"   
which -s atom && export EDITOR="atom --wait"

## GIT
#### Configurar Git
git config --global user.name "Juan Perez”   
git config --global user.email    juanperez@ejemplo.com   
git config --global core.editor “atom -w"   

## BROWSERSYNC
#### Install
npm install -g browser-sync

#### Install Gulp

npm install gulp browser-sync --save-dev

#### Start Browsersync

A basic use is to watch all CSS files in the css directory and update connected browsers if a change occurs. Navigate your terminal window to a project and run the appropriate command:

Static sites

If you’re only using .html files, you’ll need to use the server mode. Browsersync will start a mini-server and provide a URL to view your site.

browser-sync start --server --files "css/*.css"

browser-sync start --server --directory --files "*"


sudo apt install zsh
sudo apt install curl
sudo apt install git
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
chsh -s $(which zsh)
sudo apt install python3
sudo apt-get install python3-pip
sudo apt-get install python3-dev
git clone https://github.com/jblancoh/Hospital.git
sudo apt install virtualenv
virtualenv -p python3 myhosp
source bin/activate
pip install django==1.8
deactivate
sudo apt-get install postgresql
sudo apt-get install libpq-dev
sudo apt-get install apache2
sudo apt-get install python-setuptools
sudo apt-get install libapache2-mod-wsgi
source bin/activate
pip install psycopg2
pip install django-import-export
*****Crear base de datos*****
sudo su - postgres
createuser admin
psql
alter user admin with password 'postgres';
\q
python manage.py createsuperuser
python manage.py makemigrations
python manage.py migrate
python manage.py runserver 0.0.0.0:8000


sudo apt-get install gunicorn 

gunicorn hospital.wsgi:application --bind 192.168.75.128:8000

## MYSQL CONFIG ROOT(PASSWORD)
Which one-click-setup did you use? You can check the configuration files probably and find the password. 
If you can't find it, neither root without pass is working you can reset it:

Commands
```
sudo /etc/init.d/mysql stop
```
Now start up MySQL in safe mode, so you'll skip the privileges table:
```
sudo mysqld_safe --skip-grant-tables &
```
Login with root:
```
mysql -uroot
```
And assign the DB that needs to be used:
```
use mysql;
```
Now all you have to do is reset your root password of the MySQL user and restart the MySQL service:
```
update user set password=PASSWORD("YOURPASSWORDHERE") where User='root';
```
```
flush privileges;
```
quit and restart MySQL:
```
quit
```
```
sudo /etc/init.d/mysql stop
sudo /etc/init.d/mysql start
```
Now your root password should be working with the one you just set, check it with:
```
mysql -u root -p
```
Hope this will help you figure it out.
