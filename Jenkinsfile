#!groovy

pipeline {
    agent any
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
    stages {
        stage ('Build') {
            steps {
              sh 'echo "path: ${PATH}"'
              sh 'echo "M2_HOME: ${M2_HOME}"'
              sh 'mvn clean install'
            }
        }
    }
}
