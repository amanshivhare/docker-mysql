# docker-mysql

This project is about running Spring boot and MySQL with the help of Docker.
Follow the below steps to run the project.

1) Extract the project thenn unzip it.
2) Run mvn clean install.
3) Login to the Docker Hub using terminal. For that run 'docker login' followed by username and password.
    If successfully logged in then move to the next step
      else you might need to update the docker, and for that below commands might help.
      -> sudo apt update
      -> sudo apt upgrade docker-ce

4) Open the terminal and then go to the project path where Dockerfile is present i.e. 'docker-mysql'.
    Then in there build the image of the project by executing the below command.
      'docker build -t <docker-hub-username>/<image-name>:<tag> .'

Replace <docker-hub-username>, <image-name>, tag with appropriate values. (Tag as in version of the image. For ex: 0.0.1 or 0.0.3)

5) Its time to run the compose command in the same folder where docker-compose is present i.e. inside 'docker-mysql'.
    Run 'docker-compose up'.
6) Once done successfully run 'docker ps'. After this you will see 2 containers running on the local.
  -> Boot Application running on a IP:port.
  -> MySQL running on another port.
   
7) To connect to the Boot application note the IP and PORT on which its running and test it using postman.
8) Use the command 'docker exec -it <container_id> bash' to connect to the MySQL DB.
     Replace the <container_id> with appropriate id..
