# mysql-5.1.73 [![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](LICENSE)

Docker image for MySQL 5.1.73 database based on official [MySQL](https://hub.docker.com/_/mysql/) image

## Prerequisites

- Run docker commnad to get an image: `docker pull vsamov/mysql-5.1.73`
- Validate image successfully downloaded: `docker images`

## Run 

Start a **mysql** server instance
    
    # command sceleton
    $ docker run --name [name-of-image] -e MYSQL_ROOT_PASSWORD=[password] -d [name-of-image]:[tag]
    
    # command example
    $ docker run --name mysql-5.1.73 -e MYSQL_ROOT_PASSWORD=[password] -d -p 3306:3306 vsamov/mysql-5.1.73:latest

... where some-mysql is the name you want to assign to your container, my-secret-pw is the password to be set for the MySQL root user and tag is the tag specifying the MySQL version you want. See the list above for relevant tags. If port 3306 is used replace `-p 3306:3306` with `-p 3307:3306`

Container shell access and viewing **MySQL logs**:
    
    # shell script
    $ docker exec -it vsamov/mysql-5.1.73:latest bash
    
    # view logs
    $ docker logs vsamov/mysql-5.1.73:latest