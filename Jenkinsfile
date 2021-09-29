pipeline {
  agent any
  stages {
   
stage ('build'){
      steps{
        sh 'sudo docker build -t mstage:latest .'
      }
    }
   
  stage ('deploy'){
      steps{
        sh 'sudo docker run -d -p 9000:8080 mstage:latest'
      }
    }
   
     stage ('publish'){
      steps{
        sh 'sudo docker tag mstage:latest girishgmn/mstagedh:1.0'
        sh 'sudo docker login -u girishgmn -p Ggmnvnj@11aug'
        sh 'sudo docker push girishgmn/mstagedh:1.0'
      }
    }

  }
}
