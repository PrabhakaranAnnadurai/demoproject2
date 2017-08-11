pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo build'
            
          },
          "Build2": {
            sh 'echo parallel step'
            
          }
        )
      }
    }
    stage('Trigger Job') {
      steps {
        build 'build_maven'
      }
    }
  }
}