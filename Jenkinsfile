pipeline {
  agent { label 'slave3' } 
    stages {
        stage('Directory') {
            steps {
                sh 'cd /home/slave3/workspace/pipelinemaven/java-mvn-hello-world-web-app/'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
   
