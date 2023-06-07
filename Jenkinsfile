pipeline {
    agent any
    
    stages {
        stage('Clone repository') {
            steps {
                git clone https://github.com/qwertynebot/ansible.jen   
            }
        }
        
        stage('Install Ansible') {
            steps {
                sh 'pip install ansible'
            }
        }
        
        stage('Build Docker image') {
            steps {
                sh 'docker build -t darkne24/my-ansible .'
            }
        }
        
        stage('Push to Docker registry') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'docker-hub-credentials', passwordVariable: 'DOCKER_PASSWORD', usernameVariable: 'DOCKER_USERNAME')]) {
                    sh 'docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD'
                    sh 'docker push darkne24/my-ansible'
                }
            }
        }
    }
}
