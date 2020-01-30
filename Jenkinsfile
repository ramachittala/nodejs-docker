pipeline {
    agent any  
    stages {
       stage('OC Login') {
          steps {  
            sh 'oc login $CONSOLE_URL --token=$CONSOLE_TOKEN'
          }
       }
       stage('SCM CHECK'){ 
           sh 'git clone git@github.ibm.com:rchit013/nodejs-docker.git' 
       }
       stage('Build the app') {
          steps {
            sh 'oc new-build . --strategy=docker --name=nodejs-$BUILD_NUMBER'
          }
       }
    }
}
