node {
    stage('Git Checkout') {
        git branch: 'dev', url: 'https://github.com/jallu225/demo-counter-app.git'
    }
    stage('Unit Test') {
        bat 'mvn test'
    }
    stage('Integration Testing'){
        bat "mvn verify -DskipUnitTests"
    }
    stage('Maven Build'){
        bat "mvn clean install"
    }
}