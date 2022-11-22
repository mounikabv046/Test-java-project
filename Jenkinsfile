pipeline {
  agent any
  stages {
    
    stage ('build') {
      steps {
       sh '''mvn clean package'''          
      }
    }
    stage ( 'deploy' ) {
      steps {
        sshagent(['slave-tomcat']) {
      sh '''scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Build/target/simpleweb-1.0-SNAPSHOT.jar ec2-user@172.31.37.18:/opt/tomcat9/webapps'''
        }
      }
      }
      stage ( 'Test' ) {
        steps {
          sh ''' sleep 05 '''
        }
      }
  }
}

