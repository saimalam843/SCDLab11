pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        sh 'docker build -t simple-reactjs-app .'
      }
    }
    stage('Test') {
      steps {
        echo 'Tests would run here'
      }
    }
    stage('Deploy') {
      steps {
        sh 'docker run -d -p 3000:3000 simple-reactjs-app'
      }
    }
  }
}
