pipeline {
    agent { label 'slave_1' }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/nazneensyeda31/jenkins-node-demo.git'
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
