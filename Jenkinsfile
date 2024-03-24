pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/JugalC/maven-samples', branch: 'master')
      }
    }

    stage('run git bisect') {
      steps {
        sh '''git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5
git bisect run mvn verify'''
      }
    }

  }
  tools {
    maven 'ECE453m'
    jdk 'ece453'
  }
}