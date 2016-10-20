# mysql-5.1.73

Docker image for MySQL 5.1.73 database

## Prerequisites

- Run docker commnad to get an image: `docker pull vsamov/mysql-5.1.73`
- Validate image successfully downloaded: `docker images`

## Run 

Start a **mysql** server instance
    
    $ docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag
    $ docker run --name mysql-5.1.73 -e MYSQL_ROOT_PASSWORD=[password] -d vsamov/mysql-5.1.73:latest

... where some-mysql is the name you want to assign to your container, my-secret-pw is the password to be set for the MySQL root user and tag is the tag specifying the MySQL version you want. See the list above for relevant tags.




