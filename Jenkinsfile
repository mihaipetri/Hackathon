pipeline {
  agent { 
    dockerfile {
      filename 'Dockerfile.build'
      dir 'build'
    }
  }
  stages {
    stage('Clone the application repository') {
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
  }
}