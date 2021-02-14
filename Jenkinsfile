pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Stage one') {
      parallel {
        stage('Clone repo') {
          steps {
            git 'https://github.com/oisis/ansible-virtualenv.git'
          }
        }

        stage('Parallel_2') {
          steps {
            sh '''mkdir ./output
echo "test"'''
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

  }
  environment {
    VAR1 = 'value1'
    VAR2 = 'value2'
  }
}