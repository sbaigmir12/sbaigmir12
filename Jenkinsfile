pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'this is sattar'
              sh '''
                ls -latr
                pwd
                sudo yum install nodejs -y
              '''
            }
        }
     
        stage('accept') {
            steps {
                echo "Hi Good Morning"
              sh '''
                pwd
                sudo yum update -y
              '''

            }
        }
        
        stage('deploy') {
            steps {
                echo "hello sattar"
            }
        }
    }
    post {
       always {
            echo "script is successful"
       }
    
       success {
             echo "always success"
       }    
       failure {
             echo "failure"
       }
    }
}