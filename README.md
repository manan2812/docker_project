# docker_project
To Set Up Laravel, Nginx, and MySQL with Docker Compose

Prerequisites:

Before you start, you will need:

1.One Ubuntu 18.04 server

2.Docker installed

3.Docker Compose installed
With all of your services defined in your docker-compose file, you just need to issue a single command to start all of the containers, create the volumes, and set up and connect the networks:

$docker-compose up -d

When you run docker-compose up for the first time, it will download all of the necessary Docker images, which might take a while. Once the images are downloaded and stored in your local machine, Compose will create your containers. The -d flag daemonizes the process, running your containers in the background.

Once the process is complete, use the following command to list all of the running containers:

$docker ps

You will see the following output with details about your app, webserver, and db containers:

Output

CONTAINER ID          NAMES                 IMAGE                               STATUS                PORTS

c31b7b3251e0          db                    mysql:5.7.22                        Up 2 seconds          0.0.0.0:3306->3306/tcp

ed5a69704580            app                     digitalocean.com/php                  Up 2 seconds              9000/tcp

5ce4ee31d7c0          webserver             nginx:alpine                          Up 2 seconds              0
