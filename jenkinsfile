pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/python-jenkins-test.git'
            }
        }
        stage('Run Script') {
            steps {
                sh 'python app.py'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'pip install pytest'
                sh 'pytest test_app.py'
            }
        }
    }
}
