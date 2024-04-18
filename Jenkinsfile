pipeline {
    agent any

    stages {
        stage('deploy to dev') {
            when{
                branch 'dev'
            }
            steps {
                echo 'deploy to dev'
            }
        }
        stage('deploy to QA') {
            when{
                branch 'release'
            }
            steps {
                echo 'deploy to QA'
            }
            steps{
                archiveArtifacts artifacts: '**/*.war'    
            }
        }
        stage('Production Environment"') {
            when{
                branch 'master'
            }
            steps {
                echo 'Production Environment'
            }
        }
    }
}
