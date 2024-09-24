pipeline {
  agent any
  tools {
    maven 'Maven'  
  }

  stages {
    stage ('Initialize') {
      steps {
        sh '''
          echo "PATH= $PATH"
          echo "M2_HOME = ${M2_HOME}"
        '''
      }
    }
    stage ('Check Maven Version') {
      steps {
        sh 'mvn -version'
      }
    }
    stage ('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}
