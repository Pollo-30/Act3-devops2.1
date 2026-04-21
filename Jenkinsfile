pipeline {
    agent any

    stages {

        stage('Clonar repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Pollo-30/Act3-devops2.1.git'
            }
        }

        stage('Build Docker') {
            steps {
                sh 'docker build -t flask_app .'
            }
        }

        stage('Run Docker') {
            steps {
                sh '''
                docker stop flask_app || true
                docker rm flask_app || true
                docker run -d -p 5000:5000 --name flask_app flask_app
                '''
            }
        }
    }
}