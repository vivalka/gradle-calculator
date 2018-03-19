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
		   
		  
stage("Package") {
     steps {
          sh "./gradlew build"
     }
}

stage("Docker build") {
     steps {
	      sh "docker login -u nikhilnidhi -p chinki12"

          sh "docker build -t nikhilnidhi/calculator ."
     }
}

stage("Docker push") {
     steps {
          sh "docker push nikhilnidhi/calculator"
     }
}
stage("Deploy to staging") {
     steps {
          sh "docker run -d --rm -p 8765:8080 --name calculator nikhilnidhi/calculator"
     }
}

     }
}