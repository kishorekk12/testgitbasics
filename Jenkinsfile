pipeline {
  agent any
  stages {
    stage('code checkout') {
      steps {
        echo 'code checkout'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'build'
          }
        }

        stage('test') {
          steps {
            echo 'test case execution'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deployment'
      }
    }

  }
}