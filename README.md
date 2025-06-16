# Docker
# Deploying enviroments for webserver over Docker (BaseOS AWS EC2)
# Install docker-compose and setup 
  $ sudo curl -L "https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-
# After installing to make program executable 
  $ sudo chmod +x /usr/local/bin/docker-compose
# To check docker compose version run command 
  $ docker-compose --version

# Now, create a directory where we have to setup docker-compose
  $ mkdir /Docker/docker_project

# At docker_project create file named docker-compose.yml  
  $ vim docker-compose.yml (#for code details check the docker-compose.yml)

# 1st You have to check weather your system's network allowing port 8081 or not
# In Aws there is Security-Group for every EC2 instance so select your EC2's instance and in that there is "Inbound rules" where we have to insert the port 8081. 
# Follow these :
# Type: Customer TCP
# Port range: 8081
# Source: 0.0.0.0/0

# Now after all these setup now we have to run few commands in BaseOS
# Note: You must have docker running in BaseOS (To check status of docker $systemctl status docker)
# Now, run the compose (docker compose will indenity the file named docker-compose.yml and that's why we have to write code in that only)
  $ docker-compose up -d 

# Check with the browser with public IP
  $ http://public_IP:8081
