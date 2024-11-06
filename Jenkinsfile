pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'maven:3.9.9-eclipse-temurin-17' }
      }
      steps {
        sh 'mvn --version'
      }
    }
    stage('Front-end') {
      agent {
        docker { image 'node:23-alpine' }
      }
      steps {
        sh 'node --version'
      }
    }
    stage('Database'){
      agent{
        docker { image 'oraclelinux:9' }
      }
      steps{
        sh 'echo "oracle DB installed"'
      }
    }
  }
}
