pipeline {
  agent any
  stages {
    stage('one') {
      steps {
        echo 'Compile/Build the Application'
        sh 'mvn clean install'
        sleep 4
      }
    }

    stage('two') {
      steps {
        echo 'Run Unit Tests'
        sh 'mvn clean test '
        sleep 9
      }
    }

    stage('three') {
      steps {
        echo 'Package the Application'
        sh 'mvn package -DskipTests'
        sleep 7
      }
    }

  }
  tools {
    maven 'Maven 3.9.12'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}