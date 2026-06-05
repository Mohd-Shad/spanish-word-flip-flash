pipeline {
    agent {
        docker {
            image 'node:22-alpine'
        }
    }

    options {
        ansiColor('xterm')
    }

    stages {

        stage('Install') {
            steps {
                sh 'npm ci'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm run test:unit'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Mock deployment was successful!'
            }
        }
    }
}