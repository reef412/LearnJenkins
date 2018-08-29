pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                echo "Building and Installing Sandman"
            }
        }
        stage('Independent Tests') {
            steps {
                echo "Running Unit and Integration Tests"
            }
        }
        stage('Deploy') {
            steps {
                echo "Starting Sandman"
            }
        }
        stage('Dependent Integratinon Tests') {
            steps {
                echo "Running Dependent Integration Tests"
            }
        }
    }
}