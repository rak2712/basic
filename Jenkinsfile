pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/rak2712/basic.git'
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
