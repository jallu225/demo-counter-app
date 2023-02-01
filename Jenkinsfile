node {
    stage('Git Checkout') {
        git branch: 'dev', url: 'https://github.com/jallu225/demo-counter-app.git'
    }
    stage('Unit Test') {
        sh 'mvn test'
    }
}