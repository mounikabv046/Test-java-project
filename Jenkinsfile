pipeline {
  agent any
  stages {
    stage ('git') {
      steps {
        git branch: 'main', url: 'https://github.com/sandeep-kengal/Test-java-project.git'
      }
    }
    stage ('build') {
      steps {
        mvn install          
// check if the build is successful
          sh 'mvn -v'
      }
    }
  }
}
