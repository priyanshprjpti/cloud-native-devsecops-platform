pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/priyanshprjpti/cloud-native-devsecops-platform.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cloud-native-devsecops:jenkins-v1 ./app'
            }
        }

        stage('Verify Docker Image') {
            steps {
                sh 'docker image inspect cloud-native-devsecops:jenkins-v1'
            }
        }
    }
}