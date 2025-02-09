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
                def mvnHome = tool name: 'maven-3', type: 'maven'
                sh "${mvnHome}/bin/mvn package"
            }
        }
    }
}
