pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/rak2712/basic.git'
            }
        }

        stage('Install') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run with PM2') {
            steps {
                // Replace with your actual path to pm2.cmd if it's different
                bat '"C:\\Users\\Rakshith\\AppData\\Roaming\\npm\\pm2.cmd" delete all || exit 0'
                bat '"C:\\Users\\Rakshith\\AppData\\Roaming\\npm\\pm2.cmd" start app.js --name myapp'
                bat '"C:\\Users\\Rakshith\\AppData\\Roaming\\npm\\pm2.cmd" save'
            }
        }
    }
}
