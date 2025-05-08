    pipeline {
        agent { 
            docker { 
                image 'python-app-image' 
            }
        }
        stages {
            stage('Build') {
                steps {
                    bat 'docker build -t python-app-image .'
                }
            }
            stage('Run') {
                steps {
                   bat 'python hello.py'
                }
            }
        }
    }