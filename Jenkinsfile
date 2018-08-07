pipeline {
  agent {
    docker {
      image 'node:6-alpine' 
      args '-p 3000:3000' 
    }
  }
  stages {
    stage('Install dependencies') { 
      steps {
        sh 'npm install' 
      }
    }
    stage('Run tests') { 
      steps {
        sh 'npm start' 
      }
    }
  }
}