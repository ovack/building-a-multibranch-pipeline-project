pipeline {
    agent {
        docker {
            image 'node:14.15.0-alpine3.12' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
