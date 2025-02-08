pipeline {
agent any
    stages {
    stage('checkout code') {
    stepes {
        git credentialsId: '7cb25d81-e8a6-4cb8-a1fd-4b20344cd684', url: 'https://github.com/rangswamy/am.git'
    }
    }
    stage('build') {
    steps {
        sh "mvn clean package"
    }
    }
    stage('Deploy in tomcat') {     
    steps {
        deploy adapters: [tomcat9(credentialsId: '34140564-973a-4981-af37-66166d33a914', path: '', url: 'http://192.168.110.128:8086/')], contextPath: 'Amazon', war: '**/Amazon.war'
    }
}
    }
}
