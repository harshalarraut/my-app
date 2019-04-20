pipeline {
    agent any 
    stages {
        stage('Clone Repo and Clean') { 
            steps {
                 sh "mvn clean"
            }
        }
        stage('Test') { 
            steps {
                 sh "mvn test -f my-app" 
            }
        }
        stage('Deploy') { 
            steps {
                 sh "mvn package -f my-app" 
            }
        }
    }
}
