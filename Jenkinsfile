def output

pipeline {
    
   agent any
   
   tools {
	  go {'go-1.14'}
   }

   stages {
      stage('Hello') {
         steps {
             sh 'go build'
         }
      }
   }
}