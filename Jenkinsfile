pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/changliu8/docker_hello.git'
            }
        }

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
