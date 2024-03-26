pipeline {
    agent any

    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('NPM Audit') {
            steps {
                bat 'npm audit'
            }
        }
        stage('Run Integration tests') {
            steps {
                bat 'npm run test'
            }
        }
        stage('Deploy to prodution') {
            steps {
                script {
                     input("Deploy to production?") 
                }
                echo 'Deploying...'
            }
        }
    }
}