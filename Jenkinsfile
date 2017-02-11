pipeline {
  agent any

  environment {
    AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
    AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
  }

  stages {
    stage('Build') {
      steps {
        sh 'echo access key $AWS_ACCESS_KEY_ID'
        sh 'echo secret access key $AWS_SECRET_ACCESS_KEY'
        sh 'echo branch_name $BRANCH_NAME'
        sh 'echo change_id $CHANGE_ID'
      }
    }
  }
}

