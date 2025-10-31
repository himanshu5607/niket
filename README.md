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


#2
{ 
"Version": "2012-10-17", 
    "Statement": [ 
        { 
            "Sid": "PublicReadGetObject", 
            "Effect": "Allow", 
            "Principal": "*", 
            "Action": "s3:GetObject", 
            "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*" 
        } 
    ] 
} 


#3
 Search for and add the permission policy: 
AmazonEC2RoleforAWSCodeDeploy.


In the instance's terminal, install the CodeDeploy agent: 
#!/bin/bash 
sudo yum update -y 
sudo yum install ruby -y 
sudo yum install wget -y 
cd /home/ec2-user 
wget https://aws-codedeploy-us-east-1.s3.us-east-1.amazonaws.com/latest/install 
chmod +x ./install 
sudo ./install auto 
sudo service codedeploy-agent status

#8
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:PutObject",
            "Resource": "arn:aws:s3:::himbkt-08/*"
        }
    ]
}
policy:
Amazons3fullaccess
cloudwatchfullacess
AWslambdaBasicexecution


import json
import boto3
s3 = boto3.client('s3')
def lambda_handler(event, context):
    bucket = "himbkt-08"
    dataToUpload = {}
    dataToUpload["name"] = "Himanshu"
    dataToUpload["age"] = 25
    dataToUpload["profession"] = "Engineer"
    dataToUpload["address"] = "Delhi"
    dataToUpload["phone"] = "1234567890"
    dataToUpload["file"] = "himdata"
    fileName = "himdata" + ".json"
    uploadByteStream = bytes(json.dumps(dataToUpload).encode('UTF-8'))
    s3.put_object(Bucket=bucket, Key=fileName, Body=uploadByteStream)
    print('Put Complete') 
