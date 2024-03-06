pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "This is Build stage."'
                build 'PES1UG21CS164-1'
                sh 'g++ hello.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "This is Test stage."' 
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "This is Deploy stage."' 
                sh 'echo "Deployment Success" '
                sh 'echo "Deployment Failed" 
            }
        }
    }
    post{
        failure{
            error 'Pipeline Failed'
        }
    }
}