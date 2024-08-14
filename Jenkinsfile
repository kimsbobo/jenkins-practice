pipeline {
    agent {
        node {
            label 'docker-agent-2'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "Building"
                sh ''' 
                python3 -m venv /path/to/venv
                . /path/to/venv/bin/activate
                pip install fire
                deactivate
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