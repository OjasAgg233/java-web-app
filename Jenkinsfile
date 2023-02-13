pipeline {
  agent { label 'linux' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t nvyadhariwal28/java-web-app:latest .'
      }
    }
    
  stage('Push Docker Image') {
            steps {
                sh 'docker login -u nvyadhariwal28 -p parveshnvya'
                sh "docker images"
                sh 'docker push nvyadhariwal28/java-web-app:latest'
            }
        }   
   
  
  }
}
