pipeline {
    agent {
        docker {
            image 'node:18'
        }
    }

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/ShaikhSiddiqNitJ/CICDREACT.git'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build the React app') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Start the React app') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}
