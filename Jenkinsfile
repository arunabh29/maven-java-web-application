pipeline {

agent any

stages {
 
 stage ('Say Hello') {
  
  agent any
  
  steps {
  sayHello 'Awesome Student !'
    }
  }
 
 
 stage ('Git Information') {
  
  agent any
  
  steps {
   
   echo "My branch name: ${env.BRANCH_NAME}"
   
   script {
   
    def myLib = new linuxacademy.git.gitStuff();
    
    echo "My Commit: ${myLib.gitCommit("${env.WORKSPACE}/.git")}"
   
       }
     }
  }
 

 stage ('Initial') {
  steps {
  sh 'echo "Hello jenkins github pipeline test groovy script"'
    }
  }
 
 stage ('Maven build') {
  steps {
  sh 'mvn clean compile'
    }
  }
 
 
 
 
 }

}
