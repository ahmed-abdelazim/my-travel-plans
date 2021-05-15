pipeline {
    agent {
        docker {
            image 'ubuntu'
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
                sh 'pwd' 
            }
        }
    }
}
