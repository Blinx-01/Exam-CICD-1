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
                def helloContent = readFile('Hello.txt')
                echo "Content of hello.txt: ${helloContent}
                }
            }
        }
        
    }
}
