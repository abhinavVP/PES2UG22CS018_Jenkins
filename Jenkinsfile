pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh '''
                    g++ -o PES2UG22CS018-1 PES2UG22CS018-1.cpp
                    echo "Build completed successfully"
                '''
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh '''
                    ./PES2UG22CS018-1
                    echo "Testing completed successfully"
                '''
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh '''
                    echo "Deployment completed successfully"
                '''
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
    }
}
