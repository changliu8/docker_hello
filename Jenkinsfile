pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('hello-image')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('hello-image').run()
                }
            }
        }
    }
}