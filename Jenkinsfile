pipeline {
   agent any

   stages {
      stage('Build') {
         steps {
            sh label: '', script: './gradlew assembleDebug '
         }
      }
   }
}
