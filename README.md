# niket

kubernetes
sudo apt-get update && sudo apt-get upgrade -y

sudo apt-get install docker.io -y
sudo usermod -aG docker $USER
newgrp docker

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube

minikube start

minikube status


