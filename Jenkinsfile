pipeline {
    agent {
        docker {
            image 'node:14.15.0-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
        HOME = "${WORKSPACE}"
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm update && npm install'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}
