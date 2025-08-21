pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/nazneensyeda31/jenkins-node-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build & Run') {
            steps {
                sh 'npm start &'
            }
        }
    }
}
