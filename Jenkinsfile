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
          sh mv clean install
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















}
