pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Downloading project from GitHub...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building HTML, CSS and JavaScript project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing project files...'

                bat '''
                    if not exist index.html exit /b 1
                    if not exist index.css exit /b 1
                    if not exist index.js exit /b 1
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Website deployment completed!'
            }
        }
    }

    post {
        success {
            echo 'Jenkins pipeline completed successfully!'
        }

        failure {
            echo 'Jenkins pipeline failed!'
        }
    }
}
