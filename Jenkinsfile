pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o my_program my_program.cpp'
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
                sh 'cp my_program /usr/local/bin/'  // Simulated deployment
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
