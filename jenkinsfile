pipeline {
    agent any 

  stages {
        stage('Compile Stage') { 

            steps {
                withmaven(maven : 'M3') {
                   sh 'mvn clean compile'
                  }
             }
         }
    stage ('Testing Stage') { 
         
            steps {
                withmaven(maven : 'M3') {
                   sh 'mvn test'
                  }
               }
          }

     
    stage ('Deployment Stage') { 
              steps {
                withmaven(maven : 'M3') {
                   sh 'mvn deploy'
                  }      
              }
    }
 }

}
