pipeline {
    agent any

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
                sh 'javac sample.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java sample'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the job'
            }
        }
    }
}
