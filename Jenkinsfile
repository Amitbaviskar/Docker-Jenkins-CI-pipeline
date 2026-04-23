pipeline {
    agent {
        docker {
            image 'docker:latest'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Amitbaviskar/Docker-Jenkins-CI-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker ps'
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run --rm myapp'
            }
        }
    }
}
