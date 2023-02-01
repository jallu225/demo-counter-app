pipeline {
    agent any
    tools {
        maven "maven"
    }
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'dev', url: 'https://github.com/jallu225/demo-counter-app.git'   
            }
        }
        stage('UNIT Test'){
            steps {
                script {
                     sh "mvn test"
                }
            }
        }
        stage('Integration Testing'){
            steps {
                script {
                    sh "mvn verify -DskipUnitTests"
                }
            }
        }
        stage('Maven Build'){
            steps {
                script {
                    sh "mvn clean install"
                }
            }
        }
    }
}