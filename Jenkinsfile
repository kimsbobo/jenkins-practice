pipeline {
    agent {
        node {
            label 'docker-agent-2'
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
                pip install -r requirements.txt 
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Test"
                sh ''' 
                python3 hellofire.py
                python3 hellofire.py --name=Argie
                python3 hellofire.py --name=Irish
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