pipeline {
  agent any
  stages {
    stage('vcs') {
      steps {
        git url: 'https://github.com/lakshmi164585/spring-petclinic.git',
            branch: 'main'
        
            } 
    }
    stage('build') {
      steps {
        sh './mvnw package'
            }
          }
    stage('copy the file') {
      steps {
        sh 'sudo cp ${WORKSPACE}/target/spring-petclinic-3.0.0-SNAPSHOT.jar  /home/ubuntu/spc'
            }
          }
    
    stage('ansible deployment') {
      steps {
        sh 'ansible-playbook -i host spc-playbook.yaml'
            }
          } 
     } 

}
