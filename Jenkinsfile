pipeline {
  agent any
  stages {
    stage('Builds') {
      parallel {
        stage('Build') {
          steps {
            echo 'This is Build'
          }
        }

        stage('Build 2') {
          steps {
            echo 'This is my second build'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Test 2') {
      steps {
        echo 'testing 2'
      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy'
        input(message: 'Do you want to deploy', ok: 'yes, i want')
      }
    }

    stage('Final') {
      steps {
        echo 'You reached final'
      }
    }

  }
}