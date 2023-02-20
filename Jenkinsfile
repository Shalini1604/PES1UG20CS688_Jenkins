pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o shal PES1UG20CS688.cpp'
                build job : 'PES1UG20CS688-1'
                echo 'Build stage successful'
            }
        }
        stage('Test') {
            steps {
                sh './shal'
                echo 'Test stage successful'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying "'
                echo 'Deployment successful'
            }
        }
    }
    post {
        failure {
          echo 'Pipeline failed'
                }
            
        
    }
}
