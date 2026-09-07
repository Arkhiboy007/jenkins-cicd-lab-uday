pipeline {

    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Starting Build Stage...'
                bat 'python --version'
                bat 'python -m pip install -r requirements.txt'
                echo 'Build completed successfully.'
            }
        }

        stage('Test') {
            steps {
                echo 'Starting Test Stage...'
                bat 'python -m pytest tests -v'
                echo 'All tests completed successfully.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Starting Deploy Stage...'
                echo 'Application deployed successfully.'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD Pipeline failed.'
        }
    }
}