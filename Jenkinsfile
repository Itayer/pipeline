pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
        git 'git@34.77.9.203:user12/jenkins-pipeline-itayer.git'
      }
    }
    stage('test') {
      steps {
        sh 'npm test'
      }
    }
    stage('build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('archive') {
      steps {
        archiveArtifacts '*.zip'
      }
    }
  }
}