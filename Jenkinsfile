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
                echo 'Quality Gate PASSED'
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Simulating Docker build...'
                bat 'mkdir target'
                bat 'echo dummy image > target/docker-image.txt'
            }
        }

        stage('Docker Push') {
            steps {
                echo 'Simulating Docker push to DockerHub...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulating deployment...'
            }
        }
    }

    post {
        success {
            echo 'PIPELINE SUCCESS'
        }
        failure {
            echo 'PIPELINE FAILED'
        }
    }
}
