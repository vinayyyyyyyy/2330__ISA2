pipeline {
    agent any  

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    
                    bat "docker build -t vinayyy/2330 ."
                }
            }
        }
        stage('Build and Run Docker Container') {
            steps {
                script {
                    
                    bat "docker rm -f my-app-container || exit 0"

                    
                    bat "docker run -d --name my-app-container vinayyy/2330"
                }
            }
        }
    }
}
add:
clone the github repository.
delete a container named <roll_no>
