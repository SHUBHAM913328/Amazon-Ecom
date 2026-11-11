pipeline {
  agent any

  stages {
    // Clone source code from GitHub repository
   stage('clone project') {
      steps {
           git branch:'master' , url:'https://github.com/PraveenKuberABC/Amazon-Ecom.git'
       }
   }
 // Clean previous build artifacts
   stage('clean') {
      steps {
           sh 'mvn clean'
       }
   }
   // Compile the Maven project
   stage('compile') {
      steps {
           sh 'mvn compile'
       }
   }

   stage('test') {
      steps {
           sh 'mvn test'
       }
   }

   stage('build') {
      steps {
           sh 'mvn clean install'
       }
   }
   
}

}
