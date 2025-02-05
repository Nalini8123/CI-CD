pipeline {
 agent any
 
 tools {
   jdk 'jdk17'
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
          sh "mvn clean install -DskipTests"
       }
     }
       stage('Deploy') {
           steps {
            sh echo "admin" | sudo -S cp CI-CD/target/webapps.war /opt/tomcat/webapps
           }
          }
    
        stage('test') {
          steps {
           echo "testing..."
          }
        }
       }
     }
















