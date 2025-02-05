piepline {
 agent any
   stages{
     stage('checkout') {
       steps {
          checkout scm
       }
     }
     stage('build') {
       steps {
          sh "mvn clean install"
       }
     }
       stage('Deploy') {
           steps {
             sh "sudo cp CI-CD/target/webapps.war /opt/tomcat/webapps"
           }
          }
    
        stage('test') {
          steps {
           echo "testing..."
          }
        }
       }
     }
















}
