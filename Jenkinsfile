pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o my_program my_program.cpp'  // Correct compilation command
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './my_program'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the C++ application...'
                sh 'mkdir -p $HOME/bin && cp my_program $HOME/bin/'
                echo 'Deployment Successful! Executable placed in $HOME/bin/'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
