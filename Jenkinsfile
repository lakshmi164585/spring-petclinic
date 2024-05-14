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

     stage("Checkout from SCM"){
                steps {
                    git branch: 'main', credentialsId: 'github', url: 'https://github.com/lakshmi164585/jenkins_proj2'
                }
        }
    stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

       }

   }
}
