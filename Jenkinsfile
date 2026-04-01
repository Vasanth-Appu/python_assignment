pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                bat '''
                echo Checking Python path...
                C:\\Python314\\python.exe --version
                '''
            }
        }

        stage('Install Dependencies') {
            steps {
                bat '''
                C:\\Python314\\python.exe -m pip install --upgrade pip
                C:\\Python314\\python.exe -m pip install -r requirements.txt
                '''
            }
        }

        stage('Run App') {
            steps {
                bat '''
                C:\\Python314\\python.exe app.py
                '''
            }
        }

    }
}