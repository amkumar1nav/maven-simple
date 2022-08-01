pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "M3"
   }

   stages {
      stage('Compile') {
         steps {
            // Get some code from a GitHub repository 
         
            sh "mvn clean compile"
         }
         }
      stage("Test") {
          steps {
            
            sh "mvn clean test"
            
          }

      }
      stage("Deploy") {
          steps {
            
             
            sh "mvn clean install"
            
          }
          post {
              success {
                  archiveArtifacts 'target/*.jar'
              }

          }


      }

      }
   }

