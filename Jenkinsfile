pipeline {
  agent {label 'slave3'}
  stages {
   
stage ('build'){
      steps{
        sh 'pwd'
        sh 'ls'
        sh 'docker build -t mvn1:latest .'
      }
    }
     stage ('publish'){
      steps{
        sh 'docker tag mvn1:latest girishgmn/mvnnow:5.0'
        sh 'docker login -u girishgmn -p Ggmnvnj@11aug'
        sh 'docker push girishgmn/mvnnow:5.0'
      }
    }
  stage ('deploy'){
      steps{
        sh 'docker run -d -p 9000:8080 mvn1:latest'
      }
    }  
  }
}
