pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Amitbaviskar/Docker-Jenkins-CI-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run --rm myapp'
            }
        }
    }

    post {
        success {
            echo 'Build Success ✅'
        }
        failure {
            echo 'Build Failed ❌'
        }
    }
}
