pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/muneebmoon/DevOPs.git'
            }
        }

        stage('Deploy to Azure VM') {
            steps {
                script {
                    // Use sshpass to copy files to remote Azure VM
                    sh '''
                    sshpass -p 'AbaB12)(!@#$' scp -o StrictHostKeyChecking=no -r * moon@20.194.15.119:/var/www/html
                    '''
                }
            }
        }
    }
}
