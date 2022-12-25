 Devops Project
* Create EC2 instance, install jenkins and maven, set environment variable
* Integrate Git with jenkins 
    In jenkins UI go to manage plugins and install github and go to global tool configuration and check git
* Integrate Maven with jenkins
    In jenkins UI go to manage plugins and install maven integration and go to global tool configuration -add JDK and Maven path
    Once build is triggered from maven project, war file is generated in target folder /var/lib/jenkins/workspace.
    war file is artifact which is the outcome of the build.
*  Integrate Tomcat Server with jenkins
    To deploy artifact on the target environment we need the tomcat server 
    Create EC2 instance and install java/tomcat
    In jenkins UI install go to manage plugins deploy to container and manage credentials go to jenkins - global cred - add credentials
    artifacts should be copied to the tomcat server, artifacts are stored in webapp directory
* Docker
go inside container
cd webapps.dist
cp -R * ../webapps/
cd ../webapps
docker build -t mytomcat(name of the image) .



*****
docker ps - running containers
docker ps -a - shows all the containers
docker images - lists all the images
docker run -d --name tomcat-container(containername) -p 8081:8080 tomcat(image name)
--8081 is to access externally
docker exec -it tomcat-container /bin/bash - to get inside the container 
docker stop containername - stops the container
docker prune image -a - deletes all images
docker container prune -a - deletes all containers
