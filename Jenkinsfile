pipeline {
  agent {
    node {
      label 'swarm'
    }

  }
  stages {
    stage('Parallel execution') {
      parallel {
        stage('Say Hello') {
          steps {
            sh 'echo "hello world"'
          }
        }

        stage('borrar directorio') {
          steps {
            sh 'ls '
            deleteDir()
            sh 'ls'
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