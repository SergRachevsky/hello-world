pipeline {
    agent { label 'agent-sergey-csd-01' }
    stages {
        stage('Back-end') {
            agent {
                docker { 
                    image 'maven:3-alpine'
                    args '-u root:root'
                }
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            agent {
                label 'agent-sergey-csd-01'
                docker { image 'node:14-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}