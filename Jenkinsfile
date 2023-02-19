pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'g++ pes2ug20cs384_lab.cpp -o pes2ug20cs384_lab'
                echo 'build stage successful'
                build job: 'PES2UG20CS381-1'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './pes2ug20cs384_lab'
                echo 'test stage successful'
            }
        }
        stage ('Deploy')
        {
            steps
            {
                echo 'deployment successful'
            }
        }
    }
    post
    {
        failure
        {
            echo 'pipeline failed'
        }
    }
}
