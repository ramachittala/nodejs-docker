pipeline {
    agent any  
    stages {
       stage('OC Login') {
          steps {  
            sh 'oc login $CONSOLE_URL --token=$CONSOLE_TOKEN'
          }
       }
       stage('SCM CHECK'){ 
           steps {
            sh 'git clone https://github.com/ramachittala/nodejs-docker.git' 
           }
       }
       stage('Build the app') {
          steps {
            sh 'oc new-build . --strategy=docker --name=nodejs-$BUILD_NUMBER'
          }
       }
    }
}
