pipeline {
  agent {
    docker {
      image 'node:8-alpine' 
      args '-p 3000:3000' 
    }
  }
  environment {
    CI = 'true'
  }
  stages {
    stage('Install dependencies') { 
      steps {
        sh 'npm install' 
      }
    }
    stage('Run tests') {
      steps {
        sh 'npx cypress install' 
        sh 'npm start' 
      }
    }
  }
}