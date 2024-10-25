pipeline {
    agent any 

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    
                    bat "docker build -t vinayyy/docker2330 ."
                }
            }
        }
        stage('Delete Existing Container') {
            steps {
                script {
                    
                    bat "docker rm -f 2330 || exit 0"
                }
            }
        }
        stage('Build and Run Docker Container') {
            steps {
                script {
                    
                    bat "docker rm -f my-app-container || exit 0"

                    
                    bat "docker run -d --name my-app-container vinayyy/docker2330"
                }
            }
        }
    }
}
