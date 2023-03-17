pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'Running test2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy completed'
      }
    }

  }
}