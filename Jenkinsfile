pipeline {
  agent any
  stages {
    stage('Unit Test') { 
      steps {
        sh 'mvn clean test'
      }
    }
    stage('Deploy Standalone') { 
      steps {
        sh 'mvn deploy -P standalone'
      }
    }
    stage('Deploy CloudHub') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        sh 'mvn deploy -P cloudhub -Dmule.version=4.1.4 -Danypoint.username=emanishnitr2  -Danypoint.password=Man@1245' 
      }
    }
  }
}