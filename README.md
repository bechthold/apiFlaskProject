Project link (titorial): https://www.youtube.com/watch?v=LcZ9uJn8ffA

For the project we need Docker.
---------------------------------
Install docker: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04

<p>sudo apt update</p>
<p>sudo apt install apt-transport-https ca-certificates curl software-properties-common</p>
<p>curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -</p>
<p>sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"</p>
<p>apt-cache policy docker-ce</p>
<p>sudo apt install docker-ce</p>
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

<p>Run docker image with mysql:</p>
docker run --name some_mysql -e MYSQL_ROOT_PASSWORD=pass -p 3306:3306 -d mysql:latest

<p>Go to bash in mysql image:</p>
docker exec -it <container-name-or-id> bash

Form bash in the mysql container we start database with command:
<p>mysql -h127.0.0.1 -P3306 -uroot -ppass</p>

Work with database
---------------------------------
Create Database:
<p>CREATE DATABASE some_db;</p>




