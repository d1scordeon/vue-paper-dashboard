pipeline {
    agent any

    stages {
        stage('Cloning our GIT project') {
            steps {
                git url: 'https://github.com/DarciaIV/vue-paper-dashboard'
            }
        }
        stage('Preparing dependencies') {
            steps {
                sh 'ls -l'
                sh 'npm install'
            }
        }
        stage('Build project') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Archive the artifact') {
            steps {
                sh 'sudo zip -r dist dist/'
            }
        }
    }
}
