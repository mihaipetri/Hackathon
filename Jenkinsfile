pipeline {
  agent {
	docker { image 'node:8' }
  }
  
  stages {  
    stage('Cloning Git') {
      steps {
        git 'https://github.com/mihaipetri/Hackathon.git'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
	
	stage('Build the application') {
      steps {
        sh 'npm build'
      }
    }
     
    stage('Test the application') {
      steps {
         sh 'npm test'
      }
    }

    stage('Publish the application') {
      steps {
         sh 'docker build .'
      }
    }	
  }
}
