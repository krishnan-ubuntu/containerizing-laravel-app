![Docker](https://www.krish.website/static/images/files/badge.svg)

![Image](https://www.krish.website/static/images/files/laravel_with_docker.png)

Migrate your existing Laravel code base to Docker with Docker Compose. 

A simplified Docker Compose workflow to migrate your existing Laravel code base with Linux, Apache, MySQL, Memcached and Phpmyadmin for local development.

## Ports

Ports used in the project:
| Software | Port | Internal |
|-------------- | -------------- | -------------- |
| **Web application** | 8082 | 80 |
| **Phpmyadmin** | 8081 | 80 |
| **Mysql** | 8083 | 3306 |
| **Memcached** | 11211 | 11211 |

## Steps to use

### Add the files
To get started, make sure you have Docker installed on your system and Docker Compose, and then copy the following files in at respective locations in your code base. 
- docker-compose.yml
- Dockerfile
- docker/apache/000-default.conf

### Changes
Change your database, network and volume names as you desire. 

### Env changes
Make the following changes to the `.env` file.

DB_CONNECTION=mysql\
DB_HOST=db\
DB_PORT=3306\
DB_DATABASE=mywebsitedb\
DB_USERNAME=root\
DB_PASSWORD=password\

### Start the containers
Now you can start the containers with the following command. 
#### First time
`docker-compose up -d --build`
#### Generally
`docker-compose up -d`

## Reference
[Containerizing existing Laravel code base with Docker](https://www.krish.website/blog/post/containerizing-my-website-with-docker
)

