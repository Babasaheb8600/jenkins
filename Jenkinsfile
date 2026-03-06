pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
<<<<<<< HEAD
                git branch: 'main', url: 'https://github.com/Babasaheb8600/jenkins.git'
=======
                git 'https://github.com/Babasaheb8600/jenkins.git'
>>>>>>> 0a54a38 (webhook test)
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-flask-app .'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s-deployment.yaml'
            }
        }

    }
}
