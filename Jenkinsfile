pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    environment {
        HOME = '.'
    stages {
        stage('Build') { 
            steps {
                sh 'sudo npm install --unsafe-perm=true --allow-root'
            }
        }
    }
}
