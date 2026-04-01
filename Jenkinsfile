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
```

---

## What to Do Now

1. Open your repo on GitHub
2. Edit the `Jenkinsfile`
3. **Delete everything** and paste the above
4. Commit with message like `"remove environment block"`
5. Re-run the Jenkins pipeline

---

## How to Confirm It's Fixed

Once the pipeline runs, the log should show:
```
[Pipeline] withEnv       ← only ONE withEnv now
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Check Python)
[Pipeline] bat
Python 3.x.x           ← actual output appears