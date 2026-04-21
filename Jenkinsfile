pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'TU_REPO'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run app') {
            steps {
                sh 'nohup python app.py &'
            }
        }
    }
}