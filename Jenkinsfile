pipeline {
  agent java-project
  stages {
    stage ('git') {
      steps {
        git branch: 'main', url: 'https://github.com/sandeep-kengal/Test-java-project.git'
      }
    }
    stage ('build') {
      steps {
       sh ''mvn install''          
      }
    }
  }
}
