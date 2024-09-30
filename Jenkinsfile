pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building the application...'
        sh 'npm install'
        sh 'npm run build'
      }
    }
    stage('Test') {
      steps {
        echo 'Running tests...'
        sh 'npm test'
      }
    }
    stage('Package') {
      steps {
        echo 'Packaging the application...'
        sh 'zip -r build.zip .'
        archiveArtifacts artifacts: 'build.zip'
      }
    }
  }
}
