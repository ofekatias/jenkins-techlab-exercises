pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        timeout(time: 10, unit: 'MINUTES')
        timestamps()  // Timestamper Plugin
        disableConcurrentBuilds()
    }
    tools {
        jdk 'jdk11'
        maven 'maven36'
    }
    environment {
        NVM_HOME = tool('nvm')
    }
    stages {
        stage('Build') {
            steps {

                sh 'java -version'

                sh 'javac -version'

                sh 'mvn --version'

            }
        }
    }
}
