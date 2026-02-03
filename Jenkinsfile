pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/RJ-Richard-96/DevOps-K8s-Security.git'
            }
        }
        stage('build jar') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('build docker image') {
            steps {
                sh 'docker build -t javaapp:v1 .'
            }
        }
    }
}
