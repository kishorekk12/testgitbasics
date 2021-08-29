pipeline {
  agent any
  environment {
    VERSION = '2.0'
  }
  stages {
    stage('code checkout') {
      steps {
        echo "code checkout for ${VERSION}"
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
          when {
            expression {
              BRANCH_NAME = 'master'
            }
          }
          steps 
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
