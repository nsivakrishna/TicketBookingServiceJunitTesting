pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                  sh '''
                      cd /var/lib/jenkins/workspace/gitpipelinetest
                       sh './parameters.sh'
              	       
                         if [[ $(/usr/bin/pip freeze | grep awscli)  = ${awscliver} ]]; then
              
                            echo "==Expected version standard-slv aws version  $(/usr/bin/pip freeze | grep awscli) and install version same==="
              
                          else
                      
                              echo  "????????????? not expected standard-slv aws version $(/usr/bin/pip freeze | grep awscli) ?????????????"
                          fi
                        
                     '''
            }
        }


    }
}
