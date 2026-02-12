pipeline {
 agent any

 stages {

  stage('Clone'){
   steps{
    git branch: 'main', url: 'https://github.com/AnoopRahul/jenkins2.git'
   }
  }

  stage('Compile'){
   steps{
    bat 'javac Hello.java'
   }
  }

  stage('Run'){
   steps{
    bat 'java Hello'
   }
  }
 }

 post {
  success {
   archiveArtifacts '*.class'
   echo 'Build Successful'
  }
  failure {
   echo 'Build Failed'
  }
 }
}
