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

    stage('Stage 2') {
      steps {
        sh 'echo "Stage in the front of echo"'
        echo 'Step 2 in stage 2'
      }
    }

    stage('Prepare') {
      steps {
        git(url: 'https://github.com/oisis/cloudguru-training', credentialsId: 'testuser1')
      }
    }

  }
}