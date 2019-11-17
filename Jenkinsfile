pipeline {
    agent any

    options {
        timestamps()
    }

    stages {
        stage('Clean WorkSpace') {
            steps {
                cleanWs()
            }
        }

        stage('Build Project') {
            steps {
                sh 'mvn build'
            }
        }

        stage('Unit Testing') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
