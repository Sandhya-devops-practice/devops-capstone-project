# DevOps Lifecycle Implementation using Jenkins, Ansible, Docker on AWS

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
