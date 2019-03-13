# Docker Image Containing Apache, PHP, SQL Server Drivers, and XDebug Setup

## Overview
Quickstart for any development environment using PHP and SQL Server.

## Building the container
Build an image using:
```
docker build -t php-sqlsrv .
```
  
Run the container with environment variables:
```
docker run -p 80:80 \
-e XDEBUG_REMOTE_ENABLE=1 \
-e XDEBUG_REMOTE_CONNECT_BACK=0 \
-e XDEBUG_REMOTE_AUTOSTART=1 \
-e XDEBUG_REMOTE_HOST=<your-ip-address> \
-e XDEBUG_REMOTE_PORT=9000 \
--name php-sqlsrv \
-d php-sqlsrv
```

## TODO
1. Complete Environment Setup  
2. Publish to Docker Hub  