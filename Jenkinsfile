Pipeline {
    agent { node { label 'Node1' } }
    stages {
       stage('build') {
          steps {
              sh '''
                pwd
                yum update
              '''
          }
       
       }
       stage('install') {
          steps {
          
             sh '''
              ls -latr
              pwd
              sudo wget "https://releases.hashicorp.com/terraform/1.3.5/terraform_1.3.5_linux_amd64.zip"
              echo $PATH
              sudo unzip terraform_1.3.5_linux_amd64.zip -d /usr/local/bin
            '''
          }
       
       }

       stage('init') {
           steps {
              sh '''
                ls -l /usr/local/bin
                sudo yum install -y yum-utils
                sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
                sudo yum -y install terraform
              '''
           }
       }

       stage('deploy'){
           steps{
               echo 'terroform init'
           }
       }
       post {
          always {
               echo "successful"
          }
          success{
               echo "success"
          }
          failure {
              echo "failure"
          }
       
       }
    
    }

}










