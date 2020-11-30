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
      stage('Docker Push') {
      agent any
      steps {
        withCredentials([usernamePassword(credentialsId: 'dockerHub', passwordVariable: 'dockerHubPassword', usernameVariable: 'dockerHubUser')]) {
          sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPassword}"
          sh 'docker push shanem/spring-petclinic:latest'
        }
      }
    }
  }
