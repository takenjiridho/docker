# docker


## Tested on

- macOS 10.12.3
- Docker 17.06.2-ce
- Docker Compose 1.14.0
- MySQL Workbench 6.3

## Run services

```
mkdir ~/projs
cd ~/projs
git clone https://github.com/takenjiridho/docker.git db-on-docker
cd db-on-docker
mkdir data
docker-compose up

# on new terminal tab
cd ~/projs/db-on-docker
docker-compose ps
```

## Test connection - multiple options

- Test connection w/ database client on host OS using host OS ports
- Test with PHP based adminer tool that run on container - http://localhost:8080
- Test with databse clients within running containers. Examples below

```
docker-compose exec mysql-dev mysql -uroot -ppassword blogapp
docker-compose exec mysql-legacy mysql -uroot -ppassword legacyapp
docker-compose exec pgdb psql -U root -W blogapp
```

## A few useful commands

```
docker-compose stop
docker-compose rm
docker-compose rm -f
```

```
for remove cached git rm -r --cached .
```

<<<<<<< HEAD
## A few useful commands pgsql

```
\c databasename; change db
\dt; show tables
\d table_name ; describe table

ALTER TABLE profile
ADD COLUMN deleted_at time;
=======
```
show log query statment  pgsql

ALTER DATABASE blogapp
SET log_statement = 'all';
```

## Add Alias to Open file with `vscode` in the terminal

```bash
# You can now make vscode [FOLDER] in the Terminal
echo alias vscode=\"/Applications/Visual\\ Studio\\ Code.app/contents/Resources/app/bin/code\" >> ~/.zshrc

# Reload you Terminal 

source ~/.bash_profile

## If you are using zsh

source ~/.zshrc
>>>>>>> 37e1cc2e0204986487a3e66ec5ebb2f36ee2c28b
```
