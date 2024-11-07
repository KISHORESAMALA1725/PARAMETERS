pipeline {
    agent any
    parameters {
        string (name: 'USERNAME', defaultValue: 'KISHORE', description: 'Please Enter you name')
        choice (name: 'PROD/nNONPROD', choices['prod','dev','uat'], description: 'Please enter your choice')
    }
    stages {
        stage ('This is BUILD-STAGE') {
            steps {
                echo "***** THIS IS BUILD STAGE *****"
            }
        }
        stage ('This is when+parameter stage') {
            when {
                expression {
                    params.PROD/nNONPROD == 'yes'
                }
            }
            steps {
                echo "DEPLOYED TO PROD SUCCESSFULLY"
            }
        }
        stage ('DEPLOYED to DEV') {
            when 
                expression{
                    params.PROD/nNONPROD == 'dev'
                }
                steps {
                    echo "DEPLOYED TO DEV"
                }
            }

        }
    }
