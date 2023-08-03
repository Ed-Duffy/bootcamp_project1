pipeline{
  agent any
  environment {
    NEXUS_LOGIN =credentials("NEXUS_LOGIN")
    }
  stages{
    stage("Build"){
      steps{
      sh "cd myproject1"
      sh "sudo docker build -t localhost:8083/pyhtonapp"
      sh "sudo docker image ls"
    }
    }
    stage("Push"){
      sh "sudo dockee login localhost:8083 -u ${NEXUS_LOGIN_USR} -P  ${NEXUS_LOGIN_PSW}"
      }
    stage("Deploy"){
    }
  }
}
