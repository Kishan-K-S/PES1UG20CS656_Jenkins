pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS656.cpp'
                sh 'g++ -o PES1UG20CS656 PES1UG20CS656.cpp'
                echo 'build stage successfull'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS656'
                echo 'test stage successful'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment Successful'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
