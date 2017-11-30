pipeline {
  agent any
  stages {
    stage('Stage-1') {
      parallel {
        stage('Stage-1') {
          steps {
            echo 'Hello, I am from Blue Ocean'
          }
        }
        stage('Stage-1.1') {
          steps {
            echo 'I am from Stage-1.1'
          }
        }
      }
    }
    stage('Stage-2') {
      steps {
        echo 'I am from Stage-2'
      }
    }
    stage('Stage-3') {
      steps {
        build 'JavaProject-FreeStyleJob'
      }
    }
  }
}