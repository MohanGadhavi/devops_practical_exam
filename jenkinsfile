pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }
        stage('Package') {
            steps {
                sh 'pyinstaller --onefile add2vals.py'
            }
        }
    }
}
