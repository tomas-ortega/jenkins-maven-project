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

        stage('Compile Project') {
            steps {
                sh 'mvn compile -f jenkins-maven-project/pom.xml'
            }
        }

        stage('Unit Testing') {
            steps {
                sh 'mvn test -f jenkins-maven-project/pom.xml'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package -f jenkins-maven-project/pom.xml'
            }
        }
    }
}
