pipeline{
    agent any
    environment{
        name1 = "Raghu"
        name2 = "Madhavi"
        name3 = "sunny"
    }
    stages{
        stage("Build"){
            environment{
                name3 = "Sunny"
            }
            steps{
                echo "name1 ${name1}"
                echo "name2 ${name2}"
                echo "name3 ${name3}"

            }
        }
        stage('Test'){
            environment{
                name4 = "pinky"
            }
            steps{
            echo "name1 ${name1}"
            echo "name2 ${name2}"
            echo "name3 ${name3}"
            echo "name4 ${name4}"
            sh "printenv"
            }
        }
        stage("env"){
            environment{
                SOME_USERNAME_PASSWORD = credentials('usernamepassword')
            }
            steps{
            echo "SOME_USERNAME_PASSWORD ${SOME_USERNAME_PASSWORD}"
            echo "SOME_USERNAME_PASSWORD_USR ${SOME_USERNAME_PASSWORD_USR}"
            echo "SOME_USERNAME_PASSWORD_PSW ${SOME_USERNAME_PASSWORD_PWS}"
            }
        }
        
    }
}


