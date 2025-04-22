pipeline {
    agent any
    tools{
        maven 'maven3.6'
        jdk 'jdk17'
    }
          stages {
                stage('compile') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'githubtoken', url: 'https://github.com/Achhay/Boardgame.git']])
            }
        }
                stage('test') {
            steps {
                sh 'mvn test'
            }
        }
                stage('package') {
            steps {
                sh 'mvn package'
            }
        }
                stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}

