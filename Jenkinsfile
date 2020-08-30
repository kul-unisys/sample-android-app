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
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: '', reportFiles: 'build/reports/dependency-check-report.html', reportName: 'OWASP Dependency Check Report', reportTitles: ''])
         }
      }
   }
}
