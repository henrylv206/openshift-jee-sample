pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh '''# /usr/bin/bash
echo test'''
      }
    }
    stage('unit test') {
      steps {
        sleep 3
      }
    }
    stage('build') {
      steps {
        openshiftVerifyService(svcName: 'jenkins', namespace: 'test')
      }
    }
  }
}