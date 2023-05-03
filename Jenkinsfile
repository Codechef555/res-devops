pipeline {
    agent any 
    stages {
        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }
        stage('Build Image') {
            steps {
                sh "sudo docker build -t resappdev:v1 ."
            }
        }
        stage('Run Image') {
            steps {
                sh 'sudo docker run -d -p 8501:8501 --name docresapp resappdev:v1'
            }
        }
        stage('Testing') {
            steps {
                echo 'Process complete..'
            }
        }
    }
}
