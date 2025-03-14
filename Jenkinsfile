pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ Project...'
                    sh 'g++ -o PES2UG22CS488-1.out main/hello.cpp'  
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    sh 'chmod +x PES2UG22CS488-1.out' 
                    sh './PES2UG22CS488-1.out'  
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'echo "Deployment successful!"'
                }
            }
        }
    }

    post {
        failure {
            script {
                echo 'Pipeline failed! Please check the logs for errors.'
            }
        }
    }
}
