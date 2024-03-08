pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Introducing an intentional error...'
                // Modify the g++ command to introduce an error
                sh 'g++ -o output hello.cpp -nonexistent-option'
            }
        }

        // ... (rest of the stages remain the same)
    }

    post {
        failure {
            echo 'Pipeline failed. Taking necessary actions...'
            // Add actions to handle failure, e.g., sending notifications, cleanup, etc.
        }
    }
}
