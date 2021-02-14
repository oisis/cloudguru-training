pipeline {
  agent {
    docker {
      image 'python'
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
        sh 'apt install python-virtualenv libssl-dev'
      }
    }

  }
  environment {
    VAR1 = 'value1'
    VAR2 = 'value2'
  }
}