pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build completed...'
      }
    }

    stage('Test stages') {
      parallel {
        stage('Test1') {
          steps {
            echo 'running Test1'
          }
        }

        stage('Test2') {
          steps {
            echo 'running test2'
          }
        }

        stage('test3') {
          steps {
            echo 'Running Test3'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy', ok: 'Yes, I am sure')
        echo 'deploy completed'
      }
    }

    stage('Notify') {
      steps {
        echo 'New build completed successfully'
      }
    }

  }
}