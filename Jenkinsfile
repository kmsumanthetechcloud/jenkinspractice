pipeline {
    agent { label 'docker' } 
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/kmsumanthetechcloud/jenkinspractice.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Script') {
            steps {
                sh 'python app.py'
            }
        }
    }
}
