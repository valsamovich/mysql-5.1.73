# mysql-5.1.73 [![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](LICENSE) [![Docker Automated buil](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/vsamov/mysql-5.1.73/)

Docker image for MySQL 5.1.73 database based on official [MySQL](https://hub.docker.com/_/mysql/) image

## Installation

- Run docker commnad to get an image: `docker pull vsamov/mysql-5.1.73`
- Validate image successfully downloaded: `docker images`

## Run 

Start a **mysql** server instance:
    
    # general form
    $ $ docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]
    
    # example
    $ docker run -d --name mysql-5.1.73 -p 3307:3306 -e MYSQL_ROOT_PASSWORD=[password] vsamov/mysql-5.1.73:latest

... where some-mysql is the name you want to assign to your container, my-secret-pw is the password to be set for the MySQL root user and tag is the tag specifying the MySQL version you want. See the list above for relevant tags. If port 3306 is used replace `-p 3306:3306` with `-p 3307:3306`
    
Other **commands**:

    ## kill the container
    docker kill [container-id]
    
    # shell script/shell access
    $ docker exec -it vsamov/mysql-5.1.73:latest bash
    
    # viewing MySQL logs
    $ docker logs vsamov/mysql-5.1.73:latest

## Contribution

Please contribute using [Github Flow](https://guides.github.com/introduction/flow/). Create a fork, add commits, and [open a pull request](https://github.com/fraction/readme-boilerplate/compare/).
