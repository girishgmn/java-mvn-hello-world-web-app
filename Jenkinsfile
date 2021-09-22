pipeline {
  agent { label 'slave2' } 
    stages {
        stage('Directory') {
            steps {
                sh 'cd /home/slave2/workspace/javamaven/java-mvn-hello-world-web-app/'
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
   
