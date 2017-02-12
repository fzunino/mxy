pipeline {
  agent any

  environment {
    AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
    AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
  }

  stages {
    stage('Build') {
      steps {
        script {
            env.TAG = (env.CHANGE_ID == null) ? 'latest' : "pr-${env.CHANGE_ID}"
        }
        sh 'echo access key $AWS_ACCESS_KEY_ID'
        sh 'echo secret access key $AWS_SECRET_ACCESS_KEY'
        sh 'echo BRANCH_NAME $BRANCH_NAME'
        sh 'echo CHANGE_ID $CHANGE_ID'
        sh 'echo TAG $TAG'
      }
    }
    stage('Deploy') {
        steps {
            sh 'echo TAG $TAG' 
        }
    }
  }
}

