sudo apt-get update

sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt-get update

#Running docker commands as non-root user

getent group docker

sudo gpasswd -a <user> docker
  
getent group docker

#Starting and Enabling docker service

sudo systemctl enable docker

sudo systemctl start docker

  



