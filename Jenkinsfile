pipeline {
    agent any

    options {
        buildDiscarder(logRotator(numToKeepStr: '2', artifactNumToKeepStr: '1'))
    }

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

    post {
        always {
            archiveArtifacts artifacts: 'test/*.jar', fingerprint: true
        }
    }
}