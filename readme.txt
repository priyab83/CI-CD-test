Prerequisite:
Two AWS EC2 instance ( one is Jenkins Server and another is tomcat server)
Integration between Jenkins and Docker
Make sure ssh connection is already setup between for jenkins user between two AWS EC2 Instances.
Docker Pipeline Plugin

Agenda:
Create a sample application in java
Compile the project using maven
Package the project in war file
Create a Dockerfile which contains tomcat server
Push the code in the bitbucket
Create a pipeline job in Jenkins and trigger the build

Sample Application in Java
Firstly, create a sample registration and login page in jsp.

Dockerfile
create a Dockerfile using below instructions
`FROM tomcat:latest` — This is the base image that we will be using 
We can add Labels in your docker images and provide who is the Maintainer of the Dockerfile
Now we will add our generated war inside a tomcat/webapps folder which will be present inside a Docker container
Expose the port — This means that  tomcat server inside a docker container can be access on this port
At last, we are starting the tomcat service using catalina.sh file
