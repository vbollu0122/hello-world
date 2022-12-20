 Devops Project
* Create EC2 instance, install jenkins and maven, set environment variable
* Integrate Git with jenkins 
    In jenkins UI go to manage plugins and install github and go to global tool configuration and check git
* Integrate Maven with jenkins
    In jenkins UI go to manage plugins and install maven integration and go to global tool configuration -add JDK and Maven path
    Once build is triggered from maven project, war file is generated in target folder /var/lib/jenkins/workspace.
    war file is artifact which is the outcome of the build.
* Integrate Tomcat Server with jenkins
    To deploy artifact on the target environment we need the tomcat server 
    Create EC2 instance and install java/tomcat
    In jenkins UI install go to manage plugins deploy to container and manage credentials go to jenkins - global cred - add credentials
    