pipeline {
    agent {
        docker {
            image 'httpd'
            args '-v ${WORKSPACE}:/var/www/html -p 80:80'
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
