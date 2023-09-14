pipeline {
    agent any
    tools {
        jdk 'jdk17'
    }
    stages {
        stage ('Build') {
            steps {
                sh './gradlew clean build'
            }
            post {
                success {
                    sh './gradlew test'
                }
            }
        }
        stage('Docker') {
            steps {
                sh 'docker build . -t your.local.registry:5000/test/springk8s:latest'
                sh 'docker push your.local.registry:5000/test/springk8s:latest'
            }
        }
        stage('DeployK8s') {
            steps {
                sh 'kubectl apply -f k8s -n testnsspringk8s'
            }
        }
    }
}