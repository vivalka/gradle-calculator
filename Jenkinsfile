pipeline {
     agent any
     stages {
          stage("Compile") {
               steps {
                    sh "./gradlew compileJava"
               }
          }
          stage("Unit test") {
               steps {
                    sh "./gradlew test"
               }
          }
		   stage("Jacoco test Coverage Verification") {
               steps {
                    sh "./gradlew test jacocoTestCoverageVerification"
               }
          }
		  stage("Jacoco test Report") {
               steps {
                    sh "./gradlew test jacocoTestReport"
               }
          }
     }
}