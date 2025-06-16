# Docker
# Deploying enviroments for webserver over Docker (BaseOS AWS EC2)
# Install docker-compose and setup 
$sudo curl -L "https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-
# After installing to make program executable 
$sudo chmod +x /usr/local/bin/docker-compose


# After storing docker-compose.yml file in your system
# 1st You have to check weather your system's network allowing port 8081 or not
# In Aws there is Security-Group for every EC2 instance so select your EC2's instance and in that there is "Inbound rules" where we have to insert the port 8081. 
# Follow these :
# Type: Customer TCP
# Port range: 8081
# Source: 0.0.0.0/0

# Now after all these setup now we have to run few commands in BaseOS
# Note: You must have docker running in BaseOS (To check status of docker $systemctl status docker)
