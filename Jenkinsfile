pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                  sh '''
                      ls -la
              	       eval awscliversion="awscli==1.18.91"
                         if [[ $(/usr/bin/pip freeze | grep awscli)  = ${awscliversion} ]]; then
              
                            echo "==Expected version standard-slv aws version  $(/usr/bin/pip freeze | grep awscli) and install version same==="
              
                          else
                      
                              echo  "????????????? not expected standard-slv aws version $(/usr/bin/pip freeze | grep awscli) ?????????????"
                          fi
                        
                     '''
            }
        }


    }
}
