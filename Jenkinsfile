pipeline {
  agent any
  stages {
    stage('init') {
      parallel {
        stage('initialization') {
          steps {
            echo 'Hello, I am from Blue Ocean'
          }
        }
        stage('inits') {
          steps {
            echo 'I am from Stage-1.1'
          }
        }
      }
    }
    stage('code checkout') {
      steps {
        echo 'Code checkout'
        git(url: 'https://github.com/EMERDs/SampleProj', branch: 'master')
      }
    }
    stage('mvn build') {
      steps {
        build 'JavaProject-FreeStyleJob'
        echo 'Maven build'
        bat 'mvn clean install -DReleaseVersion=1.1.0'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying the package'
      }
    }
  }
}