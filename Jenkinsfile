pipeline {
    agent { label 'docker' }  // Runs on Docker Cloud agent
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/kmsumanthetechcloud/jenkinspractice.git'  // Change with your repo
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-flask-app .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 my-flask-app'
            }
        }
    }
}
