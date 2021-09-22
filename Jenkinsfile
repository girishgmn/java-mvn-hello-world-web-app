pipeline {
  agent { label 'slave1' } 
    stages {
        stage('Directory') {
            steps {
                // sh 'cd /home/slave1/workspace/Pipelinemaven/java-mvn-hello-world-web-app'
              sh 'cd ${WORKSPACE}'
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
    }
}
   
