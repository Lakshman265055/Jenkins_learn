pipeline {
    agent {
        label 'AGENT-1'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
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