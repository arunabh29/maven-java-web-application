pipeline {

agent any

stages {
 
 stage ('Say Hello') {
  
  agent any
  
  steps {
  sayHello 'Awesome Student !'
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
