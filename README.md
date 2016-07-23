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


## Postgres
#### Instalar Postgresql
sudo apt-get install postgresql
#### Instalar libpq-dev (para conectar django con postgres)
sudo apt-get install libpq-dev
#### Modificar template para modificacion de Pass 'postgres'
sudo su postgres -c "psql template1"
```
ALTER USER postgres WITH PASSWORD 'postgres';
```

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
