pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            sh label: '', script: './gradlew assembleRelease'
         }
      }
      stage('Running Unit Test') {
         steps {
            sh label: '', script: './gradlew test'
         }
      }
      stage('Running Sonar Analysis') {
         steps {
            sh label: '', script: './gradlew sonarqube'
         }
      }
      stage('Running OWASP DC Analysis') {
         steps {
            sh label: '', script: './gradlew dependencyCheckAnalyze'
         }
      }
   }
}
