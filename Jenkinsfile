pipeline {
    agent any
        

    stages {
        stage('checkout git') {
            steps {
              git credentialsId: 'a09c4289-b824-433b-8876-5e7fcfb8153a', url: 'https://github.com/jayakumar-star/am.git'
                
            }
            
        }
         stage('build') {
            steps {
                sh "mvn clean package"
            }

        }
        stage('deplyment') {
            steps {
               deploy adapters: [tomcat9(credentialsId: '47ddb324-79dd-4d27-ba75-58b62fde1e42', path: '', url: 'http://192.168.220.128:8090/')], contextPath: 'amazon', war: '**/*.war' 
            }
            
        }
        
        }
    }
