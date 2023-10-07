pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'this is sattar'
            }
        }
     
        stage('accept') {
            steps {
                echo "Hi Good Morning"
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