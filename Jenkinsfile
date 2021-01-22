pipeline {
    agent { label 'agent-sergey-csd-01' }
    stages {
        stage('Back-end') {
            agent {
                docker { 
                    label 'agent-sergey-csd-01'
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
                docker { image 'node:14-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}