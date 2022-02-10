pipeline {
    agent any
    stages {
        stage('Git SCM checkout') {
            steps {
                git credentialsId: 'Mycred', url: 'https://github.com/RiyaSriv1414/angular-8-registration-login-example.git'
            }
        }
        stage('Install dependency') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run NPM Build') {
            steps {
                bat 'npm run build'
            }
        }
        stage('Static code analysis') {
            steps {bat 'npm run-script lint'}
        }
        stage('Unit tests') {
            steps {bat 'npm run-script test'}
        }
    }
}
