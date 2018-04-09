
#********************************************************************************

#						MY DOCKER GUIDE
			
#********************************************************************************



  0.  sudo docker ps
 
  1. Install Docker on linux using the following:
  
	   ##### curl -sSL https://get.docker.com/ | sh

  2. Check your docker version using command :
    
      ##### sudo docker --version

  3. Check docker information using command
  
	   ##### sudo docker info

  4. Pull an existing docker container by using command
  
	    ##### sudo docker run hello-world
	    ##### sudo docker run -it ubuntu bash

  5. List docker images and container using command : 
  
	    ##### sudo docker image ls
    	##### sudo docker container ls --all

  6. Use docker help to get help:
  
	    ##### sudo docker --help

  7. Check the network by using the following command: 
  
	    ##### sudo docker network ls

  8. Pull the jboss container and use the interactive processes  command { -it } as below:
  
	    ##### sudo docker run -it jboss/wildfly
      
  9. To start a container in detached mode use {  -d  } as follows :
  
	    ##### sudo docker run -d jboss/wildfly

  10. To stop the container use the following :
      
      ##### sudo docker container stop {container names} or {container id}

  11. To remover a container use :
  
	    ##### sudo docker container rm  {container names} or {container id}

  12. To name your container so that its not auto generated use { --name } :
  
	  ##### sudo docker container run -it --name web jboss/wildfly bash
    
	  Note: bash command will let you manually run llinux commands on your e.g jboss server and navigate to folders

  13. To check logs for a container use :
  
	  ##### sudo docker container logs {container names}

  14. To run the container and access it on a generated port use :
  
	  ##### sudo docker container run -d --name web -P jboss/wildfly

  15. To specify a port when running a container use:
  
	  ##### sudo docker container run -d --name web -p8080:8080 jboss/wildfly

  16. To copy file from local machine to docker use the volume command {  -v  }:
  
      ##### sudo docker container run -d --name web -p8080:8080 -v`pwd`/webapp.war:/opt/jboss/wildfly/standalone/deployments/webapp.war jboss/wildfly

  17. To tail the container log use :
  
	  ##### sudo docker container logs web -f
	
  18. To start a container in docker :
  
      ##### sudo docker container start {container names}
