pipeline {
    agent any 
    options { skipDefaultCheckout() }
    stages {
        stage('Repository Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '02e74bc7-828b-4461-9a29-edef853a252b', url: 'https://github.com/harshalarraut/my-app.git']]])
            }}
        stage('Maven Clean') { 
            steps {
                 sh "mvn clean"
            }
        }
        stage('Test') { 
            steps {
                 sh "mvn test" 
            }
        }
        stage('Deploy') { 
            steps {
                 sh "mvn package" 
            }
        }
    }
}
