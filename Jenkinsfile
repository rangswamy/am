
pipeline {
agent any
    stages {
    stage('checkout code') {
    steps {
        git credentialsId: '7cb25d81-e8a6-4cb8-a1fd-4b20344cd684', url: 'https://github.com/rangswamy/am.git'
     }
    }
    stage('build') {
    steps {
        sh "mvn clean package"
    }
    }
        stage('Test PR') {
            when {
                expression {
                    return env.BRANCH_NAME ==~ /PR-\d+/
                }
            }
    }
    }
}
