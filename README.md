# Docker TYPO3 CMS Scaffold

## Table Of Contents
- [What does it do?](#What-does-it-do)
- [Requirements](#Requirements)
- [Installation](#Installation)
- [Restart Docker Container](#Restart)
- [Configuration](#Configuration)

## <a name="What-does-it-do"></a>What does it do?
This project offers an scaffold for TYPO3 CMS in a virtual machine with docker.

## <a name="Requirements"></a>Minimum Requirements

- [docker](https://www.docker.com) 1.12.0 - virtual machine
    - [docker for Linux](https://docs.docker.com/engine/getstarted/)
    - [docker for Mac](https://docs.docker.com/docker-for-mac/)
    - [docker for Windows](https://docs.docker.com/docker-for-windows/)
- [composer](https://getcomposer.org/) 1.2.0 - php dependency management tool

## <a name="Installation"></a>Installation
For the first installation you have to execute this command:
```
docker-compose up -d
```
Install the [TYPO3 CMS 6 LTS](https://composer.typo3.org/) with composer:
```
composer install
```

## <a name="Restart"></a>Restart Docker Container
```
docker-compose restart
```

## <a name="Configuration"></a>Configuration
Additional docker-compose services will be configured in `docker/docker-compose.override.yml`.

After configure the *docker-compose.override.yml* you have to execute this command:
```
docker-compose up -d
```
