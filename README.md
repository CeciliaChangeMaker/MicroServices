# Microservices with Jenkins Server

This repository is prepared for the article "Working with Microservices-1: Running a Java App that Consists of 10 Microservices on a Development Server."

## What's in Jenkins Server

- Jenkins
- Jenkins plugins
- Helm
- Docker
- Docker Compose
- Ansible
- Terraform
- Git
- kubectl
- eksctl
- Rancher CLI
- Maven
- Java 11
- AWS CLI Version 2
- Python 3
- Boto3
- SecurityGroup (Ports 80, 8080, 22)

## Necessary Role and Policies

- AmazonEC2ContainerRegistryFullAccess
- AWSCloudFormationFullAccess
- AdministratorAccess

In this article series, we will work with a Spring Boot application consisting of 10 microservices. It is a Java-based web application developed by Spring company. We will run it on Development, Testing, Staging, and Production environments using various DevOps tools, including Jenkins, Kubernetes, Helm, Docker, Docker Compose, Terraform, Rancher, Nexus Repository, Maven, Ansible, Prometheus and Grafana, GitHub, Amazon Route 53, AWS Certificate Manager, AWS EKS, AWS RDS MySQL Database, AWS S3 bucket, Selenium Jobs, and Jacoco. We will create each environment and run our application in it, step by step.

![Flow Chart](https://github.com/cmakkaya/microservices-with-db-on-dev-server/blob/main/flow-chart-for-readme.jpg)

In summary, we will do the following for each environment:

### Testing Environment

- Perform both manual and automated tests
- Package the app into JARs with Maven
- Prepare Dockerfiles for each microservice
- Create Helm charts to deploy the application to the Kubernetes Cluster
- Build Docker images with tags
- Push Helm charts into an AWS S3 bucket
- Create an AWS ECR Repo and push the images to it
- Create a Kubernetes cluster using Terraform for QA tests
- Deploy our microservices App on the Kubernetes cluster using the Helm charts
- Run Functional Tests on the QA Environment using Selenium jobs

### Staging Environment

- Create and manage Kubernetes clusters with Rancher
- Install Rancher into the cluster using the Helm chart
- Use MySQL Database for customer records
- Check the operation of our microservices app

### Production Environment

- Create and manage Kubernetes clusters with Rancher
- Use AWS RDS MySQL Database for customer records
- Set Domain Name and create an "A record" for the microservices app using AWS Route 53
- Configure TLS (SSL) certificate for HTTPS connection using AWS Certificate Manager
- Monitor the microservices apps in the cluster with Prometheus and Grafana

### Development Server

- Compile, test (with JUnit in pom.xml), build, and run the code on the container
- Install a development server using Terraform
- Create and clone a Source Code Management Repository (GitHub) to the Development Server
- Work in different branches (dev, feature, bugfix, hotfix, etc.) on GitHub for the DevOps cycle

We will do all of these steps step by step.
