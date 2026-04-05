# In this project, I implemented a complete CI/CD pipeline where Jenkins automatically triggers builds based on GitHub branch activity. I configured separate pipelines for development and production workflows to simulate a real-world environment.

## ⚠️ Challenges Faced

- Jenkins pipeline was not triggering via webhook → Resolved by correcting GitHub webhook URL and enabling trigger option in Jenkins

- Docker container was not accessible in browser → Opened port 80 in AWS Security Group

- Jenkins build failure → I faced almost 6 to 7 build failures.

- The 8th build was successful after debugging the issues

- Pipeline script and Dockerfile → Initially, I worked on pipeline scripts, and to better understand the concepts, I also built the application using a Dockerfile.

## 📊 DevOps Lifecycle Diagram

![DevOps Lifecycle](devops-lifecycle.png)

## 🏗️ Architecture Overview

- Jenkins Master handles pipeline orchestration
- Slave 1 (Test Node) runs testing stages
- Slave 2 (Production Node) handles deployment
- Docker containers are used to run the application
- AWS EC2 instances host all components

## Explanation

In this project, I set up a CI/CD workflow where:

- Code is pushed to GitHub and triggers Jenkins via webhook
- For the develop branch, Jenkins runs build and testing stages
- For the master branch, Jenkins executes the full pipeline including deployment
- Docker is used to containerize the application before deployment
- Ansible automates the setup and configuration across multiple nodes
- The application is deployed on AWS EC2 instances and verified through browser access

This setup helped me understand how automated pipelines work in real-world DevOps environments.

## 🔧 Tools Used

* Git & GitHub
* Jenkins
* Docker
* Ansible
* AWS

## 📸 Project Screenshots

### 🖥️ EC2 Instance Running

![EC2 Instance](ec2-instance.png)

### 🔗 Master Node Connection

![Master Connection](master-connection.png)

### 🔗 Slave Node 1 Connection

![Slave1 Connection](slave1-connection.png)

### 🔗 Slave Node 2 Connection

![Slave2 Connection](slave2-connection.png)


## ⚙️ Configuration Script

The required software is installed using a shell script.

Script file: [a.sh](a.sh)

## ⚙️ Configuration Setup

Ansible was installed on the master machine using a shell script and verified using the version command.

![Ansible Version](ansible-version.png)

### ⚙️ Ansible Connectivity Check

The connectivity between master and slave nodes is verified using Ansible ping module.

![Ansible Ping](ansible-ping.png)

## ⚙️ Ansible Playbook for Automation

An Ansible playbook is used to automate the installation of Java and Jenkins on the master node and Docker on the slave nodes.

Playbook file: [play.yaml](play.yaml)

### ▶️ Playbook Execution and Verification

![Playbook and Setup](playbook-run.png)

### 🐳 Docker and Java Installation on Slave machines

![Docker Version](docker-version.png)

## 🚀 Jenkins Setup and CI/CD Pipeline

Jenkins is installed and configured on the master node and accessed using the public IP address on port 8080.

It is used to automate the build, test, and deployment process in the DevOps lifecycle.

### 🏠 Jenkins Dashboard
![Jenkins Dashboard](jenkins-dashboard.png)

## 🖥️ Jenkins Distributed Nodes Setup

Jenkins is configured with multiple nodes (agents) to simulate different environments.

- Test Node: Used for testing builds (slave1)
- Production Node: Used for deployment (slave2)

These nodes are connected via SSH and managed from the Jenkins master, allowing jobs to run on specific environments using labels.

### 🚀 Production Node Configuration
![Prod Node](jenkins-prodconfig-node.png)

### 🔗 Connected Nodes
![Nodes](jenkins-test.png)

![Nodes](jenkins-prod.png)


### ⚙️ Pipeline Configuration
![Pipeline](jenkins-pipeline.png)

### 🔄 GitHub Webhook Integration

Jenkins is configured to automatically trigger the pipeline when code is pushed to GitHub using webhook integration.

![Jenkins Trigger](jenkins-trigger.png)

![Webhook](github-webhook.png)

### 🐳 Docker Configuration

A Dockerfile is used to containerize the application using Nginx.

### ▶️ Pipeline Execution
![Build](jenkins-build-status.png)

![Build](jenkins-console-output.png)

## Project Output

### Docker Container Running
![Docker](screenshots-docker.png)

### Application Output in Browser
![Browser Output](screenshots-browser.png)

## ✅ Conclusion

Through this project, I gained hands-on experience in setting up a complete CI/CD pipeline using Jenkins, Docker, and Ansible. I also understood how to manage distributed build environments and automate deployments on AWS infrastructure.

