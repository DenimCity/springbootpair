pipeline {
    agent {
        docker {
            image 'openjdk:8-jdk-alpine'
            args 'jar_file'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew build docker'
            }
        }
    }

}