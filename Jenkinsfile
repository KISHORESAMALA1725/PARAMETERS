pipeline {
    agent any
    parameters {
        string (name: 'USERNAME', defautValue: 'KISHORE', description: 'Enter your name')
        choices(name: 'DeployToPROD', choices: ['yes','no'], description: 'choose your option')  )
    }
    stages {
        stage ('this is build')
        steps{
            echo "This is build stage"
        }
        stage ('this to deploy in prod-stage') {
            when {
                expression{
                    params.DeployToPROD == 'yes'
                }
            }
            steps {
                echo "Deployment is done on PROD-ENV"
            }
        }
    }
}
