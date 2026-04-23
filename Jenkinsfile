pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Amitbaviskar/mavenprojectci.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Pipeline working ✅'
            }
        }
    }
}
