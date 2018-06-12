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
    }
    stages{
        stage('Test'){
            steps{
                sh './gradlew test'
            }
        }
    }

}