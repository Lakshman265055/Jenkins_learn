pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time:10, unit: 'SECONDS')
    }

    stages {
        stage('Build') {
            steps {
                
                echo 'Building...'
                sh 'sleep 10'
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