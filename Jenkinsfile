pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t ml-pro-app .'
            }
        }
    }
}
