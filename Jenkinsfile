pipeline {
  agent any
  stages {
    
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
