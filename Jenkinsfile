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
                echo "doing some cool build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing the crazy test stuff.. mmh crazy "
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