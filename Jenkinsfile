pipeline {
    agent {
        docker {
            image 'openjkd:8-jdk-alpine'
            args 'JAR_FILE'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew build docker'
            }
        }
   
}