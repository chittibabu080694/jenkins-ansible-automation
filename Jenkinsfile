pipeline {
    agent any
    
    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }
        
        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i inventory/hosts.ini playbooks/site.yml'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully: Ansible playbook executed via Jenkins!'
        }
        failure {
            echo 'Pipeline failed during execution.'
        }
    }
}
