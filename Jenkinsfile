pipeline {
    agent any

    stages {
        stage('Checkout from git') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vpsingh007/poc-user-list/']]])
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage("upload to s3") {
            steps {
                sh 'aws s3 sync .next/ s3://jenkins-poc-bucket/'
            }
        }
        
    }
}

