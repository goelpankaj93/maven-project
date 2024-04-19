pipeline {
    agent any
    triggers{
        pollSCM('* * * * *')
    }
    stages {
        stage('deploy to dev') {
            when{
                branch 'dev'
            }
            steps {
                echo 'deploy to dev'
                archiveArtifacts artifacts: '**/*.war'
            }
        }
        stage('deploy to QA') {
            when{
                branch 'release'
            }
            steps {
                echo 'deploy to QA'
                archiveArtifacts artifacts: '**/*.war'
            }
        }
        stage('Production Environment"') {
            when{
                branch 'master'
            }
            steps {
                echo 'Production Environment'
                archiveArtifacts artifacts: '**/*.war'
            }
        }
    }
}
