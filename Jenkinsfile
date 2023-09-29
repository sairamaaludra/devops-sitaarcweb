pipeline {
  agent any
  stages {
    stage('development') {
      agent {
        label 'at-dev-server'
      }
      environment {
        //the following needs to be set to not kill the node process
        JENKINS_NODE_COOKIE='dontkill'
      }
      steps {
        sh "npm install"
        sh "ng build --prod"
      }
    }
  }
}