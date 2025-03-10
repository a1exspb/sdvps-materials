pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ваш-логин/my-repo.git'
            }
        }
        stage('Test') {
            steps {
                sh 'go test .'
            }
        }
        stage('Build Docker') {
            steps {
                sh 'docker build -t my-go-app .'
            }
        }
    }
}
