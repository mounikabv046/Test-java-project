pipeline {
  agent {
  label 'java'
  }
  stages {
    stage ('git') {
      steps {
        git branch: 'main', credentialsId: 'git-private-repo', url: 'https://github.com/sandeep-kengal/java.git'
      }
    }
    stage ('build') {
      steps {
       sh '''mvn clean install'''          
      }
    }
    
  }
}

