pipeline {
    agent any

    parameters {
        string(name: 'Environment', defaultValue: 'Stage', description: 'Provide here an Environment name')
    }

    stages {
        stage('CloudFormation Provision') {
            steps {

                sh "aws cloudformation create-stack --stack-name myteststack1234 --template-body file://parent-stack.yaml --parameters ParameterKey=Environment,ParameterValue=params.Environment"
            }
        }
    }
}
