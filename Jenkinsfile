pipeline {
    agent {
        docker {
            image 'gradle:jdk8'
        
        }
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('Test') {
            steps{
                sh './gradlew test'
        
            }
        }
        stage('Deliver') {
            steps{
                sh 'java -jar build/libs/gs-accessing-data-jpa-0.1.0.jar'
        
            }
        }
    }
}