pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
      sh "cd myproject1"
      sh "sudo docker build -t localhost:8083/pyhtonapp ./myproject1/"
      sh "sudo docker image ls"
    }
    }
    stage("Push"){
      
    }
    stage("Deploy"){
    }
  }
}
