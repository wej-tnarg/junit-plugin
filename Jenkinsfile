#!groovy

pipeline {
    agent any
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
    stages {
        stage ('Initialize') {
            steps {
              sh '''
                  echo "path: ${PATH}"
                  echo "M2_HOME: ${M2_HOME}"
              '''
              sh 'mvn initialize'
            }
        }
        stage ('Build') {
            steps {
              sh 'mvn test-compile'
            }
        }
        stage ('Test and install') {
            steps {
                sh 'mvn install'
            }
        }
    }
}
