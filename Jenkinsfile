pipeline {
    agent any

    stages {

        Declarative: Checkout SCM  ✅

        stage('Build Docker Image') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/shivrajhudevu/QR.git'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh 'docker rm -f qr-container || true'
                    sh 'docker run -d -p 3000:3000 --name qr-container qr-app'
                }
            }
        }

    }
}