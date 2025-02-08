
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
    stage('Email') {
    steps {
        mail bcc: '', body: '''Build is over...

        Regards
        ABC
        9986803453''', cc: '', from: '', replyTo: '', subject: 'Build is over....', to: 'tech.tkr88@gmail.com'
    }
}
    }
}
