pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS636 PES1UG20CS636.cpp'
                build job : 'PES1UG20CS636-1'
                echo 'Build stage successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20MS636'
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
