pipeline {
    agent any
    environment {
        IMAGE_NAME = 'chandanviii/myphp'
    }
    stages {
        stage('Pull Docker Image') {
            steps {
                script {
                    docker.image(IMAGE_NAME).pull()
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    docker.image(IMAGE_NAME).inside {
                        // Place any commands you wish to execute inside the container here
                        sh 'php --version'
                    }
                }
            }
        }
    }
}
