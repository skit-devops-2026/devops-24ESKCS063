pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/skit-devops-2026/devops-24ESKCS063'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Student Management System...'
                bat 'bash scripts/test.sh'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Student Management System...'
                bat 'make build'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline Successful!'
        }

        failure {
            echo 'CI Pipeline Failed!'
        }
    }
}