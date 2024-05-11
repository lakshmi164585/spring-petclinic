pipeline {
  agent { labels 'jenkins_one' }
  triggers { pollSCM ('* * * * *') }
    tools {
        jdk 'JDK_17'
        maven 'MAVEN_HOME'
    }
  stages {
    stage('vcs') {
      steps {
        git url: 'https://github.com/lakshmi164585/spring-petclinic.git',
            branch: 'main'
      
           }
       }
   }
}
