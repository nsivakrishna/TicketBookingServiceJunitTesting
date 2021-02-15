pipeline {
    agent any
    stages {
        script{
            env.awscliver = "awscli==1.0.18"
            
        }
        stage('awscli version') {
            steps {
                  sh '''              	       
                         if [[ $(/usr/bin/pip freeze | grep awscli)  = ${env.awscliver} ]]; then
              
                            echo "==Expected version standard-slv aws version  $(/usr/bin/pip freeze | grep awscli) and install version same==="
              
                          else
                      
                              echo  "????????????? not expected standard-slv aws version $(/usr/bin/pip freeze | grep awscli) ?????????????"
                          fi
                        
                     '''
            }
        }


    }
}
