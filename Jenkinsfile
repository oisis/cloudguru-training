pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Stage one') {
      parallel {
        stage('Parallel_1') {
          steps {
            echo 'Parallel_1 output'
          }
        }

        stage('Parallel_2') {
          steps {
            sh 'echo "Parallel 2 echo output"'
          }
        }

      }
    }

    stage('Stage two') {
      steps {
        sh 'echo "Stage 2 - shell script"'
        echo 'Step 2, stage two, print message'
      }
    }

  }
}