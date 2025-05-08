    pipeline {
        agent { dockerfile true }
        stages {
            stage('Build') {
                steps {
                    echo "Building Docker image..."
                    bat 'docker build -t my-python-app .'
                }
            }
            stage('Run') {
                steps {
                    echo "Running Docker container..."
                    bat 'docker run my-python-app'
                }
            }
        }
    }