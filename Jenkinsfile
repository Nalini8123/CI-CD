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
            withCredentials([usernamePassword(credentialsId: 'jenkins', usernameVariable: 'USER', passwordVariable: 'PASS')]) {
            sh "echo $PASS | sudo -S cp CI-CD/target/webapps.war /opt/tomcat/webapps"
           }
          }
       }
    
        stage('test') {
          steps {
           echo "testing..."
          }
        }
       }
     }


