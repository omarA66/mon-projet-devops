pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t mon-site-devops .'
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    sh 'docker run -d -p 80:80 mon-site-devops'
                }
            }
        }
    }
}
