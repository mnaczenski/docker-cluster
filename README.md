# docker-cluster
simple cluster setup for test purposes

# setup
- just run docker-compose build in the folder where the docker-compose.yml is located
- after the images were created, you can start the servers with docker-compose up

This setup uses an nginx-server as a loadbalancer for an apache appserver (the appservers are scalable). The appservers use a php-fpm worker for executing php scripts, those are scalable too.
The database can be reached with "database" as host and 3306 as port (user: root, password: root). Please note, that the network-alias "database" will only work inside the containers, if you want to connect to the database from outside, you can use localhost.

The source-files of your application (e.g. shopware) are placed in /webdata and are located on the host-system to make the development easier.
