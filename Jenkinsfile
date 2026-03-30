pipeline {
    agent any
    tools {
        jdk 'jdk17' // Replace 'jdk17' with the Name configured in Manage Jenkins > Tools
    }
    stages {

        stage('Checkout') {
            steps {
                git branch: 'cse',
                    url: 'https://github.com/abhinav761/devops.git',
                    credentialsId: 'github-token'
            }
        }

        stage('Build') {
            steps {
                sh 'ls -ltr'
                sh 'javac Sample.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java Sample'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the job'
            }
        }
    }
}
