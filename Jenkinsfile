pipeline {
    agent any
    
    stages {
        stage('Cleanup') {
            steps {
                cleanWs() // Deletes the workspace before starting
            }
        }
        stage('Checkout') {
            steps {
                git branch: 'master', 
                    url: 'https://github.com/abhinav761/devops.git', 
                    credentialsId: 'github-token'
            }
        }
        stage('Build') {
            steps {
                sh 'javac sample.java'
            }
        }
        stage('Run/Test') {
            steps {
                sh 'java sample'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add actual deployment steps here (e.g., SCP to server or Docker push)
            }
        }
    }
    post {
        failure {
            echo 'Build failed. Check the logs and java file syntax.'
        }
    }
}
