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
     agent {label 'slave2'}
      steps{
        sh 'docker login -u girishgmn -p Ggmnvnj@11aug'
        sh 'docker pull girishgmn/mvnnow:5.0'
        sh 'docker run -d -p 9000:8080 girishgmn/mvnnow:5.0'
      }
    }  
  }
}
