# to-do-app
  https://www.jenkins.io/doc/book/installing/linux/
  
  1) Create AWS EC2 instance   (jenkinsmaster)
  1)  man yum 
     sudo yum upgrade
  3) man git
  4) sudo yum install git
  5) sudo yum install wget

  6) sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
    
  7) sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
  8) sudo yum upgrade
  
  9) sudo yum install java-11-openjdk 149m
 10) sudo yum install jenkins    82 m
 11) sudo systemctl daemon-reload

 12) sudo systemctl status jenkins
    sudo systemctl enable jenkins
 13) sudo systemctl start jenkins
 14) sudo systemctl status jenkins

 15) ipv4 + 8080
 16) sudo cat /var/lib/jenkins/secrets/initialAdminPassword
     history

 #install node js 
17) sudo dnf module install nodejs:18/common
18) cd todoapp 
19) npm install	
20) sudo mode src/index.js

21) ipv4 + 3000

22)  ps-a
23)  sudo kill -9

24)  run check | data is persisted or not 

25)  npm install pm2
26)  pm2 start "node src/index.js
27)  pm2 status
 28) pm2 restart "node src/index.js

#Docker Install
https://docs.docker.com/engine/install/centos/
 1) sudo yum upgrade
 2) sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
3) sudo yum install -y yum-utils
4) sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo     
         
5) sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
 OR
   sudo yum update
   sudo yum install docker.io -y
6) sudo systemctl status docker
7) sudo systemctl start docker
8) sudo yum install git
   sudo docker info
#  clone https://github.com/prashant169/node-todo-cicd.git
6) sudo docker build -t node-app-todo .
7) sudo docker images
   docker images | head - 5
8) docker run -dp 8000:8000 node-app-todo
docker ps  (images)
docker kill id

jenkins github integration  plugin jenkins||Setup webhuk

docker ps  (images)
docker kill id

24) Got to jenkins job
   add build step
25) Execute shell
    docker build . -t node-app-todo
    docker run -d --name node-app-container -p 8000:8000 node-app-todo
