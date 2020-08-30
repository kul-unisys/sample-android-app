pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            sh label: '', script: './gradlew assembleDebug '
         }
      }
      stage('Running Unit Test') {
         steps {
            sh label: '', script: './gradlew test '
         }
      }
   }
}
