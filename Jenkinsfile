pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t my-fastapi-app .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run my-fastapi-app pytest'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8000:8000 my-fastapi-app'
            }
        }
    }
}
