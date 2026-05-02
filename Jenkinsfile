pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                echo 'Simulating SonarQube analysis...'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t emc-app .'
            }
        }

        stage('Docker Push') {
            steps {
                echo 'Simulating Docker push...'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker run -d -p 8081:80 emc-app'
            }
        }
    }
}
