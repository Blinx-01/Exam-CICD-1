pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {  
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }

        
        stage('Read Hello.txt') {
            steps {
                script {
                    def helloContent = sh(script: 'cat Hello.txt', returnStatus: true).trim()
                    if (helloContent == 0) {
                        echo "Content of hello.txt: ${sh(script: 'cat Hello.txt', returnStdout: true).trim()}"
                    } else {
                        error "Failed to read hello.txt"
                    }
                }
            }
        }


        
    }
}
