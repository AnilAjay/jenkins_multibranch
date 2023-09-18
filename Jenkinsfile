pipeline {
   agent any
   stages {
     stage('checkout'){
       steps {
       git 'https://github.com/AnilAjay/Train-Ticket-Reservation-System.git'
       }
     }
     stage('build'){
       steps {
       sh 'mvn package'
       }
     }
     stage('deploy'){
       steps {
         sshagent(['deploy']) {
         sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/multi_loans/target/TrainBook-1.0.0-SNAPSHOT.war  ec2-user@172.31.35.58:/home/ec2-user/apache-tomcat-9.0.80/webapps/qaenv.war'
         }
       }
     }
   }     
}



