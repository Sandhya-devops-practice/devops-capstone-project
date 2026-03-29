# This project implements a complete DevOps lifecycle using CI/CD pipeline with Jenkins, Docker, Ansible, and AWS.

## 📊 DevOps Lifecycle Diagram

![DevOps Lifecycle](devops-lifecycle.png)

## Explanation

This project demonstrates the DevOps lifecycle:

* Code is stored and managed using GitHub
* When code is pushed to **develop branch**, Jenkins triggers build and testing
* When code is pushed to **master branch**, Jenkins performs build, testing, and deployment
* Docker is used to containerize the application
* Ansible is used for configuration management and setup
* The application is deployed on AWS for production use
* After deployment, the system is monitored for performance and improvements

This process repeats continuously, forming the DevOps lifecycle.

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

### ⚙️ Pipeline Configuration
![Pipeline](jenkins-pipeline.png)

### ▶️ Pipeline Execution
![Build](jenkins-build.png)





## ✅ Conclusion

This project successfully demonstrates automation of build, test, and deployment using DevOps tools and practices.

