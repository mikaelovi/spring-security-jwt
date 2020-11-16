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
      agent any
      environment {
        JBOSS_DEPLOYMENT_DIR = '/home/usltrdx/jboss-eap-7.2/standalone/deployments'
      }
      steps {
        echo 'Starting deployment'
        echo 'Copying artifact to ${JBOSS_DEPLOYMENT_DIR}'
      }
    }

  }
  tools {
    maven 'maven'
  }
  environment {
    JBOSS_DEPLOYMENT_DIR = '/home/usltrdx/jboss-eap-7.2/standalone/deployments'
  }
}