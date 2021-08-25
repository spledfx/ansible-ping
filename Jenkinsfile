pipeline {
    agent   any
    
    environment {
        ANSIBLE_PRIVATE_KEY=credentials('ssh-root')
    }
    
    stages {
        stage('version') {
            steps {
            sh '''
                ansible --version
                whoami
            '''
            }
        }
        stage('ping') {
            steps {
            sh '''
                ansible all -m ping -u root
            '''
            }
        }
    }
}
