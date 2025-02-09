pipeline {
    agent any

    stages {
        stage('SCM Checkout') {
            steps {
                git 'https://github.com/pulak1986/hello-world.git'
            }
        }

        stage('Compile Package') {
            steps {
                script {
                    // This makes sure the tool is available inside the stage
                    def mvnHome = tool name: 'maven-3', type: 'maven'
                    sh "${mvnHome}/bin/mvn package"
                }
            }
        }
         stage('Email Notification') {
            steps {
                mail bcc: '', body: '''Hi,
Welcome Jenkins Job Alert.

Thanks 
Pulak''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'kar.pulakk@gmail.com'
            }
        }
        stage('Slack Notification') {
            steps {
               slackSend baseUrl: 'https://hooks.slack.com/services/', channel: 'jenkins-pipeline-demp', color: 'good', message: 'This is Jenkins slack Demo', teamDomain: 'Academic', tokenCredentialId: 'slack-demo'
            }
        }
    }
}
