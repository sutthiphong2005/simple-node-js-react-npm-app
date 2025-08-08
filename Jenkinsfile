pipeline {
    agent {
        docker {
            image 'node:18-alpine' 
            args '--user 1000:1000' // Optional: Runs container as a non-root user
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}
