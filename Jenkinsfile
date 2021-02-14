pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('echo') {
      parallel {
        stage('Parallel_1') {
          steps {
            echo 'hello'
          }
        }

        stage('Parallel_2') {
          steps {
            sh 'echo "Stage below echo"'
          }
        }

      }
    }

    stage('Stage 2') {
      steps {
        sh 'echo "Stage in the front of echo"'
        echo 'Step 2 in stage 2'
      }
    }

  }
}