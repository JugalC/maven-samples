pipeline {
  agent any
  tools { 
      maven 'ECE453m' 
      jdk 'ece453' 
  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/JugalC/maven-samples', branch: 'master')
      }
    }

    stage('run test') {
      steps {
        sh 'mvn test'
      }
    }

  }
}
