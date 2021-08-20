pipeline {
    agent any

    stages {
        stage('Checkout from git') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'narendra', url: 'https://github.com/vpsingh007/poc-user-list.git']]])
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm build'
            }
        }
        
    }
}
