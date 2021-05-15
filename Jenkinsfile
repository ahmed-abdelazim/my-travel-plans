pipeline {
    agent none
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'httpd'
                    args '-v $WORKSPACE:/var/www/html'
                }
            }            
            steps {
                sh 'ls -laht'
            }
        }
        stage('Test') {
            agent {
                docker {
                    image 'httpd'
                    args '-v $WORKSPACE:/var/www/html'
                }
            }
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
