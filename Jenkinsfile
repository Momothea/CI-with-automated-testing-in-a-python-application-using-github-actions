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

        stage('Installing requirements') {
            steps {
                sh'pip install -r requirements.txt'
            }
        }

        stage('testing the app') {
            steps {
                sh'python -m unittest'
            }
        }

        stage('build a Docker image and test container') {
            steps {
                sh'docker build -t python_test_jk .'
                sh'docker run -d -p 5000:5000 python_test_jk'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
