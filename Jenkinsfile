pipeline {
  agent { label 'Agent1' }

  stages {
    stage('Run inside Docker container') {
      agent {
        docker {
          image 'node:latest'
          reuseNode true
        }
      }
      steps {
        sh 'node -v'
        sh 'echo "inside docker env"'
        sh 'ls -l'
      }
    }
  }
}
// basic pipeline with a single stage that runs inside a Docker container this is getting executed on agent1 
// using the 'node:latest' image. The stage prints the Node.js version, a message,