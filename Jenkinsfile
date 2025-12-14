pipeline {
    agent any

    stages {

        stage('Hello') {
            steps {
                echo 'Hello from Jenkinsfile'
            }
        }

        stage('Check Maven') {
            steps {
                sh 'mvn -version'
            }
        }
    }
}
