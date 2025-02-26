pipeline {
    agent {
        label 'docker' // Jenkins ka Docker Cloud use karega
    }
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
        stage('Run Tests') {
            steps {
                sh 'pytest test_app.py'
            }
        }
    }
}
