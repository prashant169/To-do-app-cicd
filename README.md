# to-do-app
  
  AWS EC2 Instance
  1) Create EC2 instance (jenkinsmaster)
  1)  man yum 
     sudo yum upgrade
  3) man git
  4) sudo yum install git

# Install Jenkins.

 https://www.jenkins.io/doc/book/installing/linux/
 Long Term Support release
 
  6) sudo yum install wget
    sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
    
  8) sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
  9) sudo yum upgrade
  
 10) sudo yum install java-11-openjdk         149m
 11) sudo yum install jenkins                 82 m
 12) sudo systemctl daemon-reload

 13) sudo systemctl status jenkins
    sudo systemctl enable jenkins
 14) sudo systemctl start jenkins
 15) sudo systemctl status jenkins

 
    *Note: ** By default, Jenkins will not be accessible to the external world due to the inbound traffic restriction by AWS. Open port 8080 in the inbound traffic rules as show below.
EC2 > Instances > Click on
In the bottom tabs -> Click on Security
Security groups
Add inbound traffic rules as shown in the image (you can just allow TCP 8080 as well, in my case, I allowed All traffic).
# Login to Jenkins using the below URL
 16) ipv4 + 8080
 18) sudo cat /var/lib/jenkins/secrets/initialAdminPassword
     history
Install the Docker Pipeline plugin in Jenkins:"Docker Pipeline".
 # install node js 

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

# Docker Install
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
   sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo         
5) sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
   OR
   sudo yum update
   sudo yum install docker.io -y
   
7) sudo systemctl status docker
8) sudo systemctl start docker
9) sudo yum install git
   sudo docker info
#clone https://github.com/prashant169/node-todo-cicd.git
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
