pipeline {
    agent any

    stages {
        stage('clean') {
            steps {
                bat 'mvn clean'
            }
        }
        stage('build') {
            steps {
                bat 'mvn package'
            }
        }
        stage('archive') {
            steps {
                archiveArtifacts artifacts: '**/*.war'
            }
        }
    }
}
