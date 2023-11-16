pipeline {
    agent {
        node {
            label 'docker_agent_python'
            }
      }
    triggers { pollSCM '*/5 * * * *' }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd myapp
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                cd myapp
                python3 hello.py
                python3 hello.py --name=Bonie
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "finally doing some delivery stuff.."
                '''
            }
        }
    }
}