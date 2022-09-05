pipeline {
  agent any
  stages {
    stage('compile-app') {
      steps {
        echo 'this is the compile job'
        sh 'mvn compile'
        sleep 4
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the test job'
        sh 'mvn test'
        sleep 9
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the package job'
        sh 'mvn package'
        sleep 7
      }
    }

   
  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this is the second pipeline...'
    }

  }
}
