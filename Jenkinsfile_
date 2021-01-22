pipeline {
    agent { label 'agent-sergey-csd-01' }

    stages {
        stage('Build') {
            steps {
                sh 'uptime' 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
