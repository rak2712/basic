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
                bat 'pm2 delete all || exit 0'     // Clean up any existing instances
                bat 'pm2 start app.js --name myapp'
                bat 'pm2 save'                     // Optional: saves process list
            }
        }
    }
}
