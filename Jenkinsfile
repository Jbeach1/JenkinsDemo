pipeline {
    environment {
        env = 'prod'
        
    }
    agent any
    stages {
        stage('Build'){
            steps {
                echo '... Loading appropriate configurations ...'
                echo '... Compiling some fun stuff ...'
            }
        }

        stage('Integration Tests'){
            steps {
                echo '... Passed 23/23 tests ...'
                echo '... Moving to next section ...'
            }
        }

        stage('Deploy code'){
            steps {
                echo '... Deploying code to destination ...'
                echo '... Transfer complete ...'
            }
        }

        stage('Generate Artifacts'){
            steps{
                echo '... Uploading build artifacts to artifactory'
            }
        }

        stage('Clean: ws'){
            steps {
                cleanWs()
            }
        }
    }
}