pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/Kavya-tha/apachewebsite'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t webapp-image .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 1234:8080 --name webapp-container webapp-image'
            }
        }
    }
}
