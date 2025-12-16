pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello from Jenkinsfile'
            }
        }
        stage('Maven') {
            steps {
                sh 'mvn -version'
            }
        }
    }
}
