pipeline{
    agent any
    environment{
          DEPLOY_TO = 'production'
          some_name = 'sunny'
          DEPLOY_TO_dev = 'devlop'
          version ='1.0'
    }
    stages{
        stage('Build'){
              when {
                  environment name: 'DEPLOY_TO', value: 'production'
              }
              steps{
                  echo "Code is deployed to production"
              }
        }
        stage('notdevlop'){
            when {
                    not{
                          environment name: 'DEPLOY_TO_dev', value: 'test'
                          }
                  }
             steps{
                echo "Code is deployed to test"
                }
             }
        stage('devlop'){
            when {
                      environment name: 'DEPLOY_TO_dev', value: 'test'
                  }
            steps{
                echo "Code is deployed to test"
            }
        }
        stage('sunny'){
                 when{
                  equals expected: 'sunny',actual: some_name
                    }
                  steps{
                    echo " name:${some_name}"
                  }
              }
        stage('version'){
            when {
              expression{
              version == "1.0"
               }
            }
          steps{
          echo "Building this version:${version}"
            }
          }
        stage('AlloF'){
          when{
            allOf {
                environment name: 'DEPLOY_TO' , value: 'production'
                environment name: 'version' , value: '1.0'
            }
          }
          steps{
            echo "Artifact is deployed to production with allof"
            echo "The Version ID is:  ${version}"
          }
        }
        }
}

               

