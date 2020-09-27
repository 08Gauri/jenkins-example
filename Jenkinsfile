<<<<<<< HEAD
node {
   def mvnHome
   stage('Preparation') { // for display purposes.          
      mvnHome = tool 'MAVEN_HOME'
   }
   stage('Build') {
      // Run the maven build
      withEnv(["MVN_HOME=$mvnHome"]) {
         if (isUnix()) {
            sh '"$MVN_HOME/bin/mvn" clean package'
         } else {
            bat(/"%MVN_HOME%\bin\mvn" clean package/)
         }
      }
   }
}
=======
pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn test'
                }
            }
        }

    }
}
>>>>>>> 9f3105c363da605840ae987c46e6dc057748f949
