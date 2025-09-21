pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project (simple echo)...'
                sh 'echo Build step - no build tool required!'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests (simple echo)...'
                sh 'echo Test step - no test framework!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application (simple echo)...'
                sh 'echo Deploy step - no deploy required!'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed.'
        }
    }
}
