pipeline{
    agent any
    stages{
        stage('Build'){
            agent any
                options{
                    skipDefaultCheckout()
                    }
            options{
              timestamps()
                }
            steps{
              echo "Pipline Build is done!"
              }
          
    }    
  }
}
