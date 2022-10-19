<p>Project link (titorial): https://www.youtube.com/watch?v=LcZ9uJn8ffA

For the project we need Docker.
---------------------------------
Install docker: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04

sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
apt-cache policy docker-ce
sudo apt install docker-ce
Docker should now be installed, the daemon started, and the process enabled to start on boot.

The basic command in Docker:
---------------------------------
Show all images in system:
docker images

Remove container: https://docs.docker.com/engine/reference/commandline/rm/

docker rm [NAME]

For example:
docker rm /some_mysql

We need to install mysql in Docker:
---------------------------------
docker pull mysql

Run docker image with mysql:
docker run --name some_mysql -e MYSQL_ROOT_PASSWORD=pass -p 3306:3306 -d mysql:latest

Go to bash in mysql image:
docker exec -it <container-name-or-id> bash

Form bash in the mysql container we start database with command:
mysql -h127.0.0.1 -P3306 -uroot -ppass

Work with database
---------------------------------
Create Database:
CREATE DATABASE some_db;

Enter to database:
USE some_db

Show tables:
SHOW TABLES

Create requirements.txt:
---------------------------------
pip freeze > requirements.txt

Create docker image:
---------------------------------
Go to project folder and do:
docker-compose up








