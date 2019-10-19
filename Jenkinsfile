pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Initialize') {
      steps {
        echo 'Inicnado....'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn clean test'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean package -DskipTests'
      }
    }
    stage('Finished') {
      steps {
        echo 'Finalizado'
      }
    }
  }
}