pipeline {
    agent {
        label 'jdk11'
    }
    stages {
        stage('clone') {
            steps {
                git url : "https://github.com/Manipavan98/js-e2e-express-server.git" ,
                branch : "main"
            }
        }
        stage('install') {
            steps {
                sh 'npm install'
            }
        }
        stage('run'){
            steps {
                 sh 'npm run build'
            }
        }
        stage('test'){
            steps {
                sh 'npm test'
            }
        }
    }
}