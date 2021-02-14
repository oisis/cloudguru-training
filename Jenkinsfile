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
        sh 'env | sort'
      }
    }

    stage('Stage three') {
      steps {
        git 'git@github.com/ansible-virtualenv'
      }
    }

  }
  environment {
    VAR1 = 'value1'
    VAR2 = 'value2'
  }
}