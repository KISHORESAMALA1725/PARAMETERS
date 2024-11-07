pipeline {
    agent any
    parameters {
        string (name: 'USERNAME', defaultValue: 'KISHORE', description: 'Please Enter you name')
        choice (name: 'PRODNONPROD', choices: ['prod','dev','uat'], description: 'Please enter your choice')
    }
    stages {
        stage ('This is BUILD-STAGE') {
            steps {
                echo "***** THIS IS BUILD STAGE *****"
            }
        }
        stage ('This is when+parameter stage') {
            when {
                expression{
                     params.PRODNONPROD == 'prod'
                }
            }
            steps {
                echo "DEPLOYED TO PROD SUCCESSFULLY"
            }
         stage ('this is dev stage')  {
            when {
                expression {
                    params.PRODNONPROD == 'dev'
                }
            }
            steps {
                echo "DEPLOYED TO DEV SUCCESSFULLY"
            }
         }

        }
        }
    }
