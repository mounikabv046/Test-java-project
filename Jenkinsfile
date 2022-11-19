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
       sh '''mvn clean install'''          
      }
    }
    stage ( 'deploy' ) {
      steps {
        sshagent(['tomcat-deploy']) {
           scp /var/lib/jenkins/workspace/Build/target/simpleweb-1.0-SNAPSHOT.jar ec2-user@172.31.37.18:/opttomcat9/webapps   
}
    
  }
}

