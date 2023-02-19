pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES2UG20CS384.cpp'
                sh 'g++ -o PES2UG20CS384 PES2UG20CS384.cpp'
                echo 'build stage successful'
            }
        }
        stage('Test'){
            steps{
                sh './PES2UG20CS384-1'
                echo 'Test stage executed successfully'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployed Successfully'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
