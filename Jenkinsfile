pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/chittibabu080694/jenkins-ansible-automation.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    playbook: 'playbook.yml',
                    inventory: 'inventory/hosts.ini',
                    credentialsId: 'ansible-ssh-key',
                    disableHostKeyChecking: true,
                    colorized: true
                )
            }
        }
    }
}
