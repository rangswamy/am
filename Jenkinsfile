
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
    }
    post {
        always {
            mail bcc: '', body: """'project: ${env.JOB_NAME}<br/> Build Number: ${env.BUILD_NUMBER}<br/> url: ${env.BUILD_URL}'""", cc: '', from: '', replyTo: '', subject: "'$(currentBuild.result)'", to: 'rswami90@gmail.com'
        }
    }
}
