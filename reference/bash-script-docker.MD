yum -y update
yum install docker -y
service docker status
service docker start
service docker status
docker ps
docker pull tomcat
docker images
docker run -d --name tomcat-container -p 8080:8080 tomcat:latest
docker exec -it tomcat-container /bin/bash


Inside tomcat container 
    1  ls
    2  cd webapps.dist/
    3  ls
    4  cp -R * ../webapps
    5  ls
    6  cd ..
    7  ls
    8  cd webapps
    9  ls
   10  history
