pipeline {
    agent {
    environment {
        CI = 'true'
    }
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    environment {
        HOME = '.'
  }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install --unsafe-perm=true --allow-root'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
