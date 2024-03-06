pipeline{
    agent any
        stages{
            stage('Build'){
                steps{
                    build 'PES1UG21CS557-1'
                    sh 'g++ new.cpp -o output'
                }
            }
            stage('Test'){
                steps{
                    sh './output'
                }
            }
            stage('Deploy'){
                steps{
                    echo 'Dployment Successful'
                }
            }
        }
        post {
            failure{
                echo 'Pipeline failed'
            }
        }
    
}
