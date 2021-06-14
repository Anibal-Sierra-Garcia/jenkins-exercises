pipeline {
  agent any
  stages {
    stage('Parallel execution') {
      parallel {
        stage('Say Hello') {
          steps {
            sh 'echo "hello world"'
          }
        }

        stage('build app') {
          steps {
            sh 'ci/build-app.sh'
          }
        }

      }
    }

  }
}