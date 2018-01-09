# MYSQL Docker
This is an unofficial, open-source for MYSQL based projects that run on Docker-Compose. 
    Mysql 5.6
    PhpMyAdmin
    
## Usage
You are up and running in three simple steps:
$ cd docker-mysql
$ docker-compose up --build -d 

## Backup/Restore Mysql
* Backup
  sudo docker exec -i mysql mysqldump -uroot -proot test > mysql/dumps/dump_`date +%d-%m-%Y"_"%H_%M_%S`.sql
* Restore from a backup
  sudo docker exec -i mysql mysql -u root -proot test < mysql/dumps/dump.sql
 
You can just open your browser at:

http://localhost:8080 or you can get the container IP: docker inspect CONTAINER ID | grep IPAddress
