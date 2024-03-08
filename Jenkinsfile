pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling the C++ code...'
                sh 'g++ -o output hello.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment steps here
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Taking necessary actions...'
            // Add actions to handle failure, e.g., sending notifications, cleanup, etc.
        }
    }
}
