pipeline {
    environment {
        ENV = 'stage'
        //changes
    }
    agent any
    stages {

        stage('Approval'){
            when {
                expression { ENV == 'prod' }
            }
            steps {
                echo '... Escalating approval ...'
                echo '... Requires 2 approvers ...'
            }
        }
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

                // echo '... Passed 21/23 tests ...'
                // error('...Failed to pass integration tests ...')
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