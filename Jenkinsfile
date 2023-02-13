pipeline {

    agent none  stages {
  	stage('Maven Install') {
    	agent {
      	docker {
        	image 'maven:3.5.0'
        }
      }
      steps {
      	sh 'mvn clean install'
      }
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
}
