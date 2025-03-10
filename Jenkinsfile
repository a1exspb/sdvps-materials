
pipeline {
    agent {
        docker {
            image 'golang:1.24.1' // Укажите нужную версию Go
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/a1exspb/sdvps-materials.git'
            }
        }
        stage('Test') {
            steps {
                sh 'go test .'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
    }
}
