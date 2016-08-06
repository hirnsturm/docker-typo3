# Docker TYPO3 CMS Scaffold

## Table Of Contents
- [Requirements](#Requirements)
- [Installation](#Installation)
- [Restart Docker Container](#Restart)
- [Import a SQL-Dump](#Import-SQL-Dump)
- [Configuration](#Configuration)

## <a name="Requirements"></a>Requirements
For running [docker](https://www.docker.com) containers you have to download and install it:
- [docker for Linux](https://docs.docker.com/engine/getstarted/)
- [docker for Mac](https://docs.docker.com/docker-for-mac/)
- [docker for Windows](https://docs.docker.com/docker-for-windows/)

## <a name="Installation"></a>Installation
For the first installation you have to execute this command:
```
docker-compose up -d
```
## <a name="Restart"></a>Restart Docker Container
```
docker-compose restart
```
## <a name="Import-SQL-Dump"></a>Import a SQL-Dump
Username, password and database can be configured individually (see (Configuration)[#Configuration]).
```
docker cp {path}/{dump}.sql dwidb_mysql_1:/tmp/db-imports/{dump}.sql && \
docker exec -it dwidb_mysql_1 mysql -u{user} -p {database} -e "source /tmp/db-imports/{dump}.sql"
```

## <a name="Configuration"></a>Configuration
Additional docker-compose services will be configured in `docker/docker-compose.override.yml`.

After configure the *docker-compose.override.yml* you have to execute this command:
```
docker-compose up -d
```
