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
                sh 'mvn package'
            }
        }
    }
}
