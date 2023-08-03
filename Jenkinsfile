pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
      sh "cd my_project1"
      sh "sudo docker build -t localhost:8083/pyhtonapp ./my_project1/"
      sh "sudo docker image ls"
    }
    }
  }
}
