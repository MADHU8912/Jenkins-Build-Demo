pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking source code from git hub'
            }
        }

        stage('Check Files') {
            steps {
                bat 'dir'
            }
        }

        stage('Build Report') {
            steps {
                bat 'echo Jenkins build successful > jenkins-report.txt'
                bat 'type jenkins-report.txt'
            }
        }
    }

    post {
        success {
            echo 'Jenkins pipeline completed successfully'
        }
        failure {
            echo 'Jenkins pipeline failed'
        }
    }
}