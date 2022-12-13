pipeline {
    agent any
    stages {
        stage('Preparation') {
         steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/VinenTik/jenkins3.git']]])
                sh'''git checkout main'''
                sh '''git pull'''
            }
        }
        stage('Build') {
           steps {
                sh 'echo "Build"'
             sh 'javac Hello.java'
            } 
        }
        stage('Test') {
         steps {
                sh 'echo "Test"'
                sh 'java Hello'
            }
        }
    }
}
