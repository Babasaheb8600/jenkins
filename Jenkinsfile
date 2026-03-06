pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Babasaheb8600/jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-flask-app:1.0 .'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s-deployment.yaml'
            }
        }

    }
}
