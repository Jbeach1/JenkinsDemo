pipeline {
    environment {
        env = 'test'
    }
    agent { any }

    stages {
        stage('Prepare Deployment Environment'){
            steps {
                    echo 'loading appropriate configurations'
                    //use some conditional logic here
            }
        }

        stage('Deploy code'){
            steps {
                echo 'gathering needed files'
                echo 'deploying code'
            }
        }

        stage('Run tests'){
            steps{
                echo 'running tests'
                //if failed abort 
            }
       
        }

        stage('Clean: ws'){
            steps {
                cleanWs()
            }
        }
    }
}