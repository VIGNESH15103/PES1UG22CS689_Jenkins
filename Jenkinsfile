pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the C++ program
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                // Run the executable
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add actual deployment steps if needed
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
