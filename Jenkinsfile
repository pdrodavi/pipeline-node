pipeline {
  agent any
  
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/pdrodavi/pipeline-node.git'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Test') {
      steps {
         sh 'npm test'
         junit 'test-results/**/*.xml'
      }
    }      
  }
}
