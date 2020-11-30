pipeline {
  agent none
  stages {
    stage('index show') {
      steps {
        echo "file"
      }
    }
    stage('Docker Build') {
      agent any
      steps {
        sh 'docker build -t rupsdan/webapp .'
      }
    }
  }
}
