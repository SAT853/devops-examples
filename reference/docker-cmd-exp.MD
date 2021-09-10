docker start -a -i `docker ps -q -l`
Explanation:

docker start start a container (requires name or ID)
-a attach to container
-i interactive mode
docker ps List containers
-q list only container IDs
-l list only last created container


Docker Run :->

docker container run -d -p 8090:8080 -v jenkinsvol1:/var/jenkins_home --name Jenkins-local jenkins/jenkins:lts
