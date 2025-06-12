pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                // Replace with your actual credentials ID
                git url: 'git@github.com:ALLANTILAK/Aws-Cloud-Formation.git',
                    credentialsId: 'github-ssh-key',
                    branch: 'main'
            }
        }

        stage('Copy to /home/ubuntu') {
            steps {
                sh '''
                sudo cp -r * /home/ubuntu/
                sudo chown -R ubuntu:ubuntu /home/ubuntu/
                '''
            }
        }
    }
}
