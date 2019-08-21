pipeline {
  agent any
  stages {
    stage('Unit Test') { 
      steps {
        bat 'mvn clean test'
      }
    }
    stage('Deploy CloudHub') { 
      steps {
        bat 'clean package deploy -DmuleDeploy'
      }
    }
  }
}