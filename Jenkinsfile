pipeline {
    agent {
        docker {
            image 'httpd'
            args '-v $WORKSPACE:/var/www/html'
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
                sh """
                    pwd
                    cd /var/www/html
                    ls
                    pwd
                  """  
            }
        }
    }
}
