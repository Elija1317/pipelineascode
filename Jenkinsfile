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
        stage('devlop'){
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
                version == "1.0"
            }
            steps{
                echo "Building this version:${version}"
            }
        }
    }
}


