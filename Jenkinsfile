pipeline {
    agent { label 'test' }

    stages {

        stage('Clone Code') {
            steps {
                git url: 'https://github.com/Sandhya-devops-practice/devops-capstone-project.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing application'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker stop myapp || true'
                sh 'docker rm myapp || true'
                sh 'docker run -d -p 80:80 --name myapp myapp'
            }
        }
    }
}
