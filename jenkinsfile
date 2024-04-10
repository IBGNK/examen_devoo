pipeline {
  agent any
  tools {
    maven "maven"
  }

  environment {
      def mvn = tool 'maven'
  }

  stages {
    stage('Git Check out') {
      steps{
        checkout scm
      }
    }

    stage('Build avec Maven') {
      steps {
        sh "${mvn}/bin/mvn clean package "
      }
    }
  }
}