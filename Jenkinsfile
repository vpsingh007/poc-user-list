pipeline {
agent any
stages {
  stage('Checkout code from github for Build') {
    steps {
      sh 'mvn -B clean verify'
    }
    } 
  }
}
