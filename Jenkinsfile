pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Build with Maven') {
            steps {
                echo 'Building project with Maven...'
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t student-app:latest .'
            }
        }
    }

    post {
        success {
            echo '✅ CI + Docker build succeeded'
        }
        failure {
            echo '❌ Pipeline failed'
        }
    }
}
