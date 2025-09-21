pipeline {
    agent any

    tools {
        maven 'Maven 3.9'  // This refers to the Maven name configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project with Maven...'
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests with Maven...'
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging the application...'
                sh 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // You can add custom deploy commands here
                // For example: sh 'scp target/*.jar user@server:/deploy/path'
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
