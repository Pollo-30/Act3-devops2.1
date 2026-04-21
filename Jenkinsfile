pipeline {
    agent any

    stages {

        stage('Install dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run app') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}