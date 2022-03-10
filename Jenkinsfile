 pipeline {
    agent any
    stages {
        stage('gitclone') {
            steps { 
                sh'''npm i'''
                sh'''npm run build'''
            }
        }
        stage('Deploy') {
            steps{
              sshagent(credentials : ['barath']) {
              sh 'ssh -o StrictHostKeyChecking=no ubuntu@35.154.129.57'
              sh 'scp -p -r /var/lib/jenkins/workspace/my-work@2 ubuntu@35.154.129.57:/var/www/html'
              }
            }
        }
    }
}
