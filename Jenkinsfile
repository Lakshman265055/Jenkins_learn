pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        //timeout(time:10, unit: 'SECONDS')
        disableConcurrentBuilds()
        //retry(1)
    }
    parameters {
        string(name: 'USERNAME', defaultValue: 'admin', description: 'Enter your username')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run test cases?')
        choice(name: 'ENVIRONMENT', choices: ['DEV', 'QA', 'PROD'], description: 'Select the deployment environment')
    }

    stages {
        stage('Build') {
            steps {
                
                echo 'Building...'
                //sh 'sleep 10'
                
               
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                //error 'pipeline failed'
            }
        }
        stage('print params'){
            steps{
                echo "Username: ${params.USERNAME}"
                echo "Run Tests: ${params.RUN_TESTS}"
                echo "Environment: ${params.ENVIRONMENT}"
            }
        }
    }
    post{

        always{
            echo "this always runs"
            deleteDir()
        }
        success{
            echo "this section runs when pipeline success"
        }
        failure{
            echo "this section run when pipeline failure"
        }
    }
}