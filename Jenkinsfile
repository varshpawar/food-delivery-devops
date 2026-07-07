pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/varshpawar/food-delivery-devops.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t food-app .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker run -d -p 8080:80 food-app || true'
            }
        }
    }
}
