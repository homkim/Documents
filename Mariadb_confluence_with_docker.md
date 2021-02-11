# Confluence with MariaDB 

## How to install mariadb
```
docker pull mariadb
docker run -d -p 3306:3306 --name mariadb -v <myPath>:/var/lib/mysql mariadb
docker logs -f --tail=20 mariadb
```
## Create database and Get IP Address of mariadb
```
docker exec -it mariadb
mysql -uroot -p
create database confluence;
quit;

apt update
apt install net-tools
ifconfig
```

## How to install confluence
```
docker pull atlassiasn/confluence
docker run -d -p 18090:8090 --name confluence -v <myPath>:/opt/atlassian/applacation-data/confluence atlassiasn/confluence
docker exec -it confluence
```

## Finish setup
* Open web page http://localhost:18090  with your browser.
* General setup
* Database setup: 
  * database type: mysql
  * IP Address: upper IP Address of mariadb
  * port: 3306
  * database name: confluence

-fin
