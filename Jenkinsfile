pipeline{
    agent any
    stages{
        stage('Build Tag'){
            when{
              changelog '.*sample_text.*'
            }
            steps{
            echo "Building master branch with tag 1.0"
            }
        }
    }
}
