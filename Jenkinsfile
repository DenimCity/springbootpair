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
                sh 'docker run -p 8080:8080 -t pairio/gs-accessing-data-jpa'
        
            }
        }
    }
}