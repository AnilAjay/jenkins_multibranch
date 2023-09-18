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
   }
}

