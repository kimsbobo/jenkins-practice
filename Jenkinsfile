pipeline {
    agent {
        node {
            label 'docker-agent-1'
        }
    }
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building"
                sh ''' 
                echo "Building some stuff" 
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Test"
                sh ''' 
                echo "Testing some stuff" 
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy"
                sh ''' 
                echo "Deploying to the moooon" 
                '''
            }
        }
    }
}