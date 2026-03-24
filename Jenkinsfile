pipeline {
    agent any

    stages {

       stage('Clone Code') {
    steps {
        git branch: 'main', url: 'https://github.com/shivrajhudevu/QR.git'
    }
}

        stage('Build Docker Image') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/shivrajhudevu/QR.git'
                }
            }
        }

        stage('Run Container') {
    steps {
        bat 'docker run -p 3000:3000 qr-app'
    }
}

    }
}