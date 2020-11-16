pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Starting build'
        sh 'mvn clean install -DskipTests'
        echo 'Build completed successfully'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Starting deployment'
        echo 'Copying artifact to ${JBOSS_DEPLOYMENT_DIR}'
      }
    }

  }
  tools {
    maven 'maven'
  }
}