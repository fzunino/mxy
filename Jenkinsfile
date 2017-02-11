pipeline {
  agent any

  environment {
    AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
    AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
  }

  stages {
    stage('Build') { 
      steps { 
        ansiColor('xterm') {
          sh 'echo build'
        }
      }
    }
    stage('Test'){
      steps {
        ansiColor('xterm') {
          sh 'echo test'
        }	
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo access key $AWS_ACCESS_KEY_ID'
        sh 'echo secret access key $AWS_SECRET_ACCESS_KEY'
      }
    }
  }
}

