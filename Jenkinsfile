pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('echo') {
      parallel {
        stage('echo') {
          steps {
            echo 'hello'
          }
        }

        stage('Stage below echo') {
          steps {
            sh 'echo "Stage below echo"'
          }
        }

      }
    }

    stage('Stage in the front of echo') {
      steps {
        sh 'echo "Stage in the front of echo"'
      }
    }

  }
}