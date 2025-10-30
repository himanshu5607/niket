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



terraform
create files with teraa.tf
create IAM user

provider "aws" {
  access_key = "AKIA4YEGL443D6HXMP"
  secret_key = "871dvU/6EGjRLg+EoVHXD1Ke8DMUnjMxTFBp"
  region     = "us-east-1"
}

resource "aws_instance" "qw_42_tera" {
  ami           = "ami-0360c520857e3138f"
  instance_type = "t3.micro"
}

terraform init
terraform plan
terraform apply

enter value: yes
and check on instance

after showing maam click terraform destroy

SONARQUBE 
http://localhost:9000/


