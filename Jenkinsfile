pipeline {
    agent any  

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    // Clone the GitHub repository
                    bat "git clone https://github.com/vinayyyyyyyy/2330__ISA2.git"
                }
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    // Build the Docker image
                    bat "docker build -t vinayyy/2330 ."
                }
            }
        }
        stage('Delete Existing Container') {
            steps {
                script {
                    // Delete container with the name <roll_no> if it exists
                    bat "docker rm -f 2330 || exit 0"
                }
            }
        }
        stage('Build and Run Docker Container') {
            steps {
                script {
                    // Delete the 'my-app-container' if it exists and run a new container
                    bat "docker rm -f my-app-container || exit 0"
                    bat "docker run -d --name my-app-container vinayyy/2330"
                }
            }
        }
    }
}
