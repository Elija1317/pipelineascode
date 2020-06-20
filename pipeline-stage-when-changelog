pipeline{
    agent any
    stages{
        stage('Build Tag'){
            when{
              changelog '.*sample_text.*'
            }
            steps{
            echo "Building is executing based on change log"
            }
        }
    }
}
