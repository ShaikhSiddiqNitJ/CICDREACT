pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/ShaikhSiddiqNitJ/CICDREACT.git'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Start') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}
