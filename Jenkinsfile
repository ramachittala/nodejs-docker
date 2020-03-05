pipeline {
    agent any  
    stages {
       stage('OC Login') {
          steps {  
            sh 'docker build .'
            sh 'ls -lthr'
            sh 'echo $PWD'
          }
       }     
    }
}
