pipeline {
  agent {label: slave3
  stages {
   
stage ('build'){
      steps{
        sh 'pwd'
        sh 'ls'
        sh 'docker build -t mstage:latest .'
      }
    }
   
  stage ('deploy'){
      steps{
        sh 'docker run -d -p 9000:8080 mstage:latest'
      }
    }
   
     stage ('publish'){
      steps{
        sh 'docker tag mstage:latest girishgmn/mstagedh:1.0'
        sh 'docker login -u girishgmn -p Ggmnvnj@11aug'
        sh 'docker push girishgmn/mstagedh:1.0'
      }
    }

  }
}
