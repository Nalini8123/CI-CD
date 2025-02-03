pipeline {
 agent any

  tools {
     jdk 'jdk'
     maven '3.9.9'
  }
 
   stages{
     stage('checkout') {
       steps {
          checkout scm
       }
     }
     stage('build') {
       steps {
          sh 'mvn clean install'
       }
     }
    
       stage('deploy') {
        steps {
         echo "deploying...."
        }
       }
        stage('test') {
          steps {
           echo "testing..."
          }
        }
       }
     }
