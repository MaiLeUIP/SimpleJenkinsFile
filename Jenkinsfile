pipeline {
    agent any

    stages{
        stage('Prepairing'){
            steps {
                echo "Pulling... ${env.BRANCH_NAME}"
                checkout scm
            }
        }

        stage('Dev'){
            when {
                branch 'dev'
            }
            steps{
                echo "The pipeline is triggered from Dev branch."
            }
        }

        stage('Test'){
            when {
                branch 'release'
            }
            steps{
                echo "The pipeline is triggered from Test branch."
            }            
        }

        stage('Prod'){
            when {
                branch 'main'
            }
            steps{
                echo "The pipeline is triggered from Prod branch."
            }
        }
    }
}
