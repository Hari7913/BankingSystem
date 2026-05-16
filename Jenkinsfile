pipeline {
    agent any

    tools {
        jdk 'jdk21'
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'master',
                credentialsId: 'git-creds',
                url: 'https://github.com/Hari7913/BankingSystem.git'
            }
        }

        stage('Build') {
            steps {
                sh 'find src -name "*.java" > sources.txt'
                sh 'javac @sources.txt'
            }
        }
    }
}
