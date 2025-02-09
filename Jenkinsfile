pipeline {
    agent any

    stages {
        stage('Clone Project') {
            steps {
                git branch:'master',url:'https://github.com/gurramnaresh26/AmazonNaresh' 
            }
        }
        stage('Clean project') {
            steps {
                sh 'mvn clean'
            }
        }
       stage('Validate') {
            steps {
                sh 'mvn validate' 
            }
        }
       stage('Compile') {
            steps {
                sh 'mvn compile' 
            }
        }
       stage('Test') {
            steps {
                sh 'mvn test' 
            }
        }
      stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
       stage('Install') {
            steps {
                sh 'mvn install' 
            }
        }

 }
    }


    
