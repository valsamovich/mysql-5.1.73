# mysql-5.1.73

Docker image for MySQL 5.1.73 database

## Prerequisites

- Run docker commnad to get an image: `docker pull vsamov/mysql-5.1.73`
- Validate image successfully downloaded: `docker images`

## Run 

Start a **mysql** server instance
    
    $ docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag
    $ docker run --name mysql-5.1.73 -e MYSQL_ROOT_PASSWORD=[password] -d -p 3306:3306 vsamov/mysql-5.1.73:latest

... where some-mysql is the name you want to assign to your container, my-secret-pw is the password to be set for the MySQL root user and tag is the tag specifying the MySQL version you want. See the list above for relevant tags. If port 3306 is used replace `-p 3306:3306` with `-p 3307:3306`

Container shell access and viewing **MySQL logs**:
    
    # shell script
    $ docker exec -it vsamov/mysql-5.1.73:latest bash
    
    # view logs
    $ docker logs vsamov/mysql-5.1.73:latest





