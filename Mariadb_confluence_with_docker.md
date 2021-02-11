# MariaDB
```
docker pull mariadb
docker run -d -p 3306:3306 --name mariadb -v <myPath>:/var/lib/mysql mariadb
docker exec -it mariadb
docker logs -f --tail=20 mariadb
```
