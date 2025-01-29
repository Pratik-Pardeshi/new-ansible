pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Pratik-Pardeshi/ansible-simple.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook playbook.yml'
            }
        }

        stage('Deploy to Web Server') {
            steps {
                sh 'cp index.html /var/www/html/index.html'
            }
        }
    }
}
