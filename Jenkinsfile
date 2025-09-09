pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/my-node-app.git'
            }
        }
        stage('Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run') {
            steps {
                bat 'start /B npm start' // start app in background on Windows
            }
        }
    }
}
