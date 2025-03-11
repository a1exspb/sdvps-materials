pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/a1exspb/sdvps-materials.git'
            }
        stage('Test') {
            steps {
                sh 'go test .'
            }
        }
    }
}
