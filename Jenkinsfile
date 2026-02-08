pipeline {
    agent any
    environment {
        USER_NAME = "Kishore_Kumar"
    }
    stages {
        stage('Build & Quality') {
            steps {
                echo "Starting Build for ${env.USER_NAME}"
                bat 'python --version'
            }
        }
        stage('Unit Test') {
            steps {
                echo 'Running Logic Test...'
                bat 'python demo.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Simulation: Deploying to Production Server...'
            }
        }
    }
    post {
        success {
            echo 'NOTIFICATION: Pipeline Finished Successfully!'
        }
        failure {
            echo 'NOTIFICATION: Pipeline Failed! Please check logs.'
        }
    }
}