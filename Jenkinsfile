 pipeline {
    agent any
    stages {
        stage('gitclone') {
            steps { 
                sh''apt install httpd'''
                sh'''run index.html'''
            }
        }
      }
   }
