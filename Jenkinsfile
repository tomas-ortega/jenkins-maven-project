pipeline {  
    agent { 
        node { 
                label 'master' 
             } 
    }

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
                sh 'mvn build ./jenkins-maven-project'
            }
        }

        stage('Unit Testing') {
            steps {
                sh 'mvn test ./jenkins-maven-project'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package ./jenkins-maven-project'
            }
        }
    }
}
