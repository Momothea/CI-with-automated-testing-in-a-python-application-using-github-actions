pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        
        stage('version') {
            steps {
                sh'python --version'
                sh'pwd'
            }
        }

        stage('Building and running') {
            steps {
                sh'pip install -r requirements.txt'
                sh'python app.py'
            }
        }

        stage('testing the app') {
            steps {
                sh'python -m unittest'
            }
        }

        
        
        stage('Deploy') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
