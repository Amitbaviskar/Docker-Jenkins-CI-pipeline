pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'id'
                sh 'sudo docker ps || docker ps'
                sh 'sudo docker build -t myapp . || docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'sudo docker run --rm myapp || docker run --rm myapp'
            }
        }
    }
}
