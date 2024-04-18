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
                archiveArtifacts artifacts: '**/myapp-1.0.0-RC.war'
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
