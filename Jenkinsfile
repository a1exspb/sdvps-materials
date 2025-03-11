pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/a1exspb/sdvps-materials.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build . -t localhost:8080/hello-world:v$BUILD_NUMBER'
            }
        }
    }
}
