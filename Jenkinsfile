pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('Test') {
      steps {
        sh '\'mvn Test\''
      }
    }

    stage('Package') {
      steps {
        sh '\'mvn package\''
      }
    }

    stage('Archive Artifcat') {
      steps {
        archiveArtifacts 'target/*.jar'
      }
    }

    stage('Publish result') {
      steps {
        junit '**/*.xml'
      }
    }

  }
}