Docker Confluence with mariadb
==================================

# How to install mariadb

## create container
```
docker pull mariadb
docker run -d -p 3306:3306 --name mariadb -e MYSQL_ROOT_PASSWORD=root -v <localpath>:/var/lib/mysql mariadb
```

## show logs
```
docker logs -f --tail=20 mariadb
```

## create confluence db
```
docker exec -it mariadb bash

apt update
apt install vim
vi /etc/mysql/my.cnf

...
[mysqld]
character-set-server=utf8mb4
collation-server=utf8mb4_bin
transaction-isolation=READ-COMMITTED
...

mysql -uroot -p
create database confluence;
```

## if necessary
Login to the confluence db and update the parameters.


## get ip address
```
apt install net-tools
ifconfig
```

# How to install confluence
```
docker pull atlassian/confluence-server
docker run -d -p 18090:8090 --name confluence -v <localpath>:/opt/atlassian/applacation-data/confluence atlassian/confluence-server
```

## copy mariadb jdbc connector
```
docker exec -it confluence bash
cp /opt/atlassian/applacation-data/confluence/*.jar /opt/atlassian/confluence/confluence/WEB-INF/lib/
ll /opt/atlassian/confluence/confluence/WEB-INF/lib/m*.jar
exit
docker restart confluence
```

## continue setup confluence with browser.
. Open web page http://localhost:18090 with your browser.
. General setup
. Database setup:
    database type: mysql
    IP Address: upper IP Address of mariadb
    port: 3306
    database name: confluence







