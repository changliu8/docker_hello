    pipeline {
        agent {
            docker {
                image 'python:3.9-slim'
				args '-u 0'
            }
        }
        stages {
            stage('Build') {
                steps {
                    echo 'Building the Docker image...'
                    bat 'docker build -t my-python-app .'
                }
            }
            stage('Run') {
                steps {
                    echo 'Running the Python script...'
                    bat 'python hello.py'
                }
            }
        }
    }