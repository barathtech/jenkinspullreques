node{
    stage('build') {
        sh'''apt install nodejs'''
        sh'''apt install npm'''
        sh'''npm i -g pm2'''
    }
    stage('git clone') {
       git 'https://github.com/barathtech/jenkinspullreques.git'
    }
    stage('release') {
        sh 'pm2 start index.js'
    }
}
