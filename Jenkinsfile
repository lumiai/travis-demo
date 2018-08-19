pipeline {
  agent {
    docker {
      image 'python'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'python hello.py'
      }
    }
    stage('Random word test') {
      parallel {
        stage('Random word test') {
          steps {
            sh 'echo "string1"'
            sh 'echo "string2"'
          }
        }
        stage('Random number test') {
          steps {
            sh 'echo 1'
            sh 'echo 2'
          }
        }
      }
    }
  }
}