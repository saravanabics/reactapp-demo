pipeline {
    agent any
    stages {
        stage('SCM') {
            steps {
                git url: 'https://github.com/saravanabics/reactapp-demo.git'
            }
        }
        stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv('sonar_scanner') 
            }
        }
        stage('Build') {
            steps {
                sh npm install
                sh npm run build
            }
        }