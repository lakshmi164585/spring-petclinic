pipeline {
  agent any
  triggers { pollSCM ('* * * * *') }
    tools {
        jdk 'JAVA_17'
        maven 'MVN_HOME'
    }
  stages {
    stage("Cleanup Workspace"){
                steps {
                cleanWs()
                }
        }

    stage('vcs') {
      steps {
        git url: 'https://github.com/lakshmi164585/spring-petclinic.git',
            branch: 'main'
      
           }
       }
   }
}
