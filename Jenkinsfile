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
        bat 'mvn clean install deploy -Dmule.version=4.1.4 -Danypoint.username=emanishnitr2  -Danypoint.password=Man@1245 -Danypoint.environment=Sandbox'
      }
    }
  }
}