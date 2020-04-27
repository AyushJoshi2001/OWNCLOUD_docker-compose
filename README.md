# ***OwnCloud_docker-compose***
 
 This is a multicontaier docker project or docker-IAAS(infrastructer as a service) running on the top of #Red_Hat_Enterprise_Linux_8 (RHEL8) . In this project the ownCloud container is attached with mysql database. And with a one single command $(docker-compose up -d) the whole infrastructer will launch.

# OwnCloud:

ownCloud is a self-hosted file sync and share server. It provides access to your data through a web interface, sync clients or WebDAV while providing a platform to view, sync and share across devices easily—all under your control. ownCloud’s open architecture is extensible via a simple but powerful API for applications and plugins and it works with any storage.
          
# Requirements:
1. The latest version of Docker (can be downloaded here: https://docs.docker.com/engine/installation/)
2. Docker compose (can be downloaded here: https://docs.docker.com/compose/install/)

# About:
By running the single command $(docker-compose up -d) your complete infrastructer will launch. Given docker-compose.yml file will automatically pull the ownCloud:latest + mysql:5.7 images and create persistant storage which will save your data. If your containers will crash there will be no data loss because of persistent volume and it will automatically set the port 8080 by using Port Address Translation (PAT). This whole process will take place with a single command.

# Installation:
              - go to your host OS. In my case Red Hat Enterprise Linux 8.
              - Download and install docker and docker-compose from the above links. 
              - Run the command:
                                systemctl start docker
              - After that run:
                                docker-compose up -d
              - wait for it to initialize completely.
After completing above steps your OwnCloud infrastructer with mysql:5.7 database will launch.

# How to use:
  
 After launching the ownCloud infrastructer simply go to your host OS and open web-browser and search:
                 http://localhost:8080 or http://host-ip:8080
                            
 For stopping the containers go to terminal.
 Run the command:
 
                docker-compose stop
  
