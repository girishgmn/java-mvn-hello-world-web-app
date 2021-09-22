pipeline {
  agent { label 'pipelinemaven' } 
    stages {
        stage('Directory') {
            steps {
                sh 'cd /home/slave2/workspace/pipelinemaven/java-mvn-hello-world-web-app/'
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
   
