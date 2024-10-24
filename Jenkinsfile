pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                script {
                    // Correct way to build a Docker image
                    sh 'docker build -t myimage .'
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    // Correct way to run a Docker container in daemon mode
                    sh 'docker run -d --name mycontainer myimage'
                }
            }
        }
    }
}
