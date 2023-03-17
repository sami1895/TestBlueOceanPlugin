pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
        retry(count: 3)
        sh 'www'
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
        input(message: 'are you sur to deploy', ok: 'yes, i\'m sure ')
        echo 'Deploy completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New build compleded successfully'
      }
    }

  }
}