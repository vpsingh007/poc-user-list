pipeline {
agent any
stages {
  stage('Checkout code from github for Build') {
    steps {
      checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vpsingh007/poc-user-list.git/']]])
    }
    } 
  }
}
