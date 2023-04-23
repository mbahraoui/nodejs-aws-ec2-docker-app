# Node.js AWS EC2 Docker Application

This is a sample Docker containerized Node.js application that is designed to run on an AWS EC2 instance.

## Getting Started

To get started with this application, you will need to have access to an AWS EC2 instance and have Docker installed on your local machine.

1. Clone this repository to your local machine:

`git clone https://github.com/mbahraoui/nodejs-aws-ec2-docker-app`


2. Build the Docker image using the provided Dockerfile:

`docker tag nodejs-aws-ec2-docker-app your-docker-username/nodejs-aws-ec2-docker-app`
`docker push your-docker-username/nodejs-aws-ec2-docker-app`

4. Launch an AWS EC2 instance and install Docker:

`ssh -i your-ec2-key-pair.pem ec2-user@your-ec2-instance-ip`
`sudo yum update -y`
`sudo amazon-linux-extras install docker -y`
`sudo service docker start`


5. Pull the Docker image from Docker Hub :
`docker pull your-docker-username/nodejs-aws-ec2-docker-app`


6. Run the Docker container on the AWS EC2 instance:

`docker run -p 80:80 -d nodejs-aws-ec2-docker-app`


7. Access the application via a web browser or API:

`http://your-ec2-instance-ip`


