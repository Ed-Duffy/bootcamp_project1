pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
      sh "sudo docker build -t localhost:8083/pyhtonapp ./myproject1/"
      sh "sudo docker image ls"
    }
    }
  }
}