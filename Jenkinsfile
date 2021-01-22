pipeline {
    agent { label 'agent-sergey-csd-01' }
    stages {
        stage('Back-end') {
            agent {
                docker { 
                    image 'ansible:ansible'
                }
            }
            steps {
                sh 'ansible-playbook -i inventory/localhost dev-servers.os-versions.yml'
            }
        }
    }
}