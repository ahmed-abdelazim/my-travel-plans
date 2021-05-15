pipeline {
    agent {
        docker {
            image 'python:rc-alpine3.13'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') {
            steps {
                sh 'ls -laht'
            }
        }
        stage('Test') { 
            steps {
                sh 'python -v' 
            }
        }
    }
}
