pipeline {
  agent {
	docker { image 'node:10' }
  }
  stages {  
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
  }
}
