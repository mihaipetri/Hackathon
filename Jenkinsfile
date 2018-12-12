pipeline {
  agent {
	label 'my-node-label'
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
	stage('Publish the application') {
      steps {
         sh 'docker build -t hackathon-app:$BUILD_NUMBER .'
      }
    }
  }
}
