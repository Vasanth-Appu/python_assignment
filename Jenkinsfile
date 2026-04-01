pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                bat "python --version"
            }
        }

        stage('Install Dependencies') {
            steps {
                bat "pip install -r requirements.txt"
            }
        }

        stage('Debug Path') {
            steps {
                bat "where python"
            }
        }

        stage('Run App') {
            steps {
                bat "python app.py"
            }
        }

    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
